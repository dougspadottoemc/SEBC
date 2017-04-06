# 1. Yarn lab

Besides the hardware details, I adjusted the cores for OS to 1

I also gave almost all the nodes' resources only to YARN, given I still don't have many other services in the cluster.

About the workload factor with my configuration, I noticed that the suggested number of mappers and reducers on the gateway (clients) changes depending on the workload factor. It depends on the number of cores and memory, and number of nodes and the workload factor.

