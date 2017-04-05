``` #!/bin/sh

CPU=4
WORKERS=4
MAX_RAM=8
DRIVES=1
AM_MB=1024
DATA_GB=10
DATA_IN=hdfs://hdfsdsemcha/user/dougspadottoemc/terasort-in
DATA_OUT=hdfs://hdfsdsemcha/user/dougspadottoemc/terasort-out
MR_MB=$(echo "scale=2; (${MAX_RAM}*1024^2 * ${WORKERS} - ${AM_MB}) / ${WORKERS}" | bc | awk -F'.' '{print $1}')

for i in 32M 64M # HDFS BLOCK SIZE
do
    for j in 4 8 16 32 64 # CONTAINERS
    do
        CNT_BND=$((${CPU}/${DRIVES}<2,${CPU}/${DRIVES},2)) #2
        CNT_TOT=$((${CNT_BND}*${DRIVES}*${WORKERS})) #8
        CNT_MAX=$((${CNT_TOT}>${j}?${j}:${CNT_TOT})) #will only go up to 8
        CNT_MB=$(echo "scale=2; (${MAX_RAM}*${WORKERS}*1024^2/${CNT_MAX})/(1024)" | bc | awk -F'.' '{print $1}')
        JVM_MB=$(echo "scale=2; (${CNT_MB}*1.2)"         | bc | awk -F'.' '{print $1}')
        DATA=$(echo "scale=2;   (${DATA_GB}*1024^3/100)" | bc | awk -F'.' '{print $1}')
        echo "HDFS Block Size: ${i}"
        echo "Bound #: ${CNT_BND}"
        echo "Containers: ${CNT_MAX}"
        echo "Memory/Container: ${CNT_MB} / ${JVM_MB}"
        echo "Data Size: ${DATA}"
        echo "Teragen"
        time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen \
            -Ddfs.blocksize=${i} \
            -Ddfs.replication=1 \
            -Dio.file.buffer.size=131072 \
            -Dmapreduce.job.maps=${CNT_MAX} \
            -Dmapreduce.map.cpu.vcores=1 \
            -Dmapreduce.map.java.opts=-Xmx${JVM_MB}m \
            -Dmapreduce.map.memory.mb=${CNT_MB} \
            -Dmapreduce.task.io.sort.mb=256 \
            -Dyarn.app.mapreduce.am.resource.mb=${AM_MB} \
            ${DATA} \
            ${DATA_IN} > out.txt 2>&1
        echo "Terasort"
        time hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort \
            -Ddfs.blocksize=${i} \
            -Dio.file.buffer.size=131072 \
            -Dmapreduce.map.java.opts=-Xmx${JVM_MB}m \
            -Dmapreduce.map.memory.mb=${CNT_MB} \
            -Dmapreduce.task.io.sort.factor=100 \
            -Dmapreduce.task.io.sort.mb=768 \
            -Dmapreduce.job.reduces=${CNT_MAX} \
            -Dmapreduce.reduce.cpu.vcores=1 \
            -Dmapreduce.reduce.java.opts=-Xmx${JVM_MB}m \
            -Dmapreduce.reduce.memory.mb=${CNT_MB} \
            -Dmapreduce.terasort.output.replication=1 \
            -Dyarn.app.mapreduce.am.resource.mb=${AM_MB} \
            ${DATA_IN} \
            ${DATA_OUT} > out.txt 2>&1

            hdfs dfs -rm -R -skipTrash ${DATA_IN} ${DATA_OUT}

            echo "${i}, ${CNT_MAX}, ${CNT_MB}, $(grep 'CPU time spent (ms)' out.txt | awk -F'=' '{print $2}')" >> results.txt
    done
done ```
