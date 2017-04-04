# 1. System Configuration Checks

## 1. Swappiness
* set to 1
![Swappiness](png/p_swappiness.PNG "Swappiness")

## 1. Mounts
![Mounts](png/p_mounts.PNG "Mounts")

1. Disable THP
* set to never
* set even after reboots
![THP](png/p_thp.PNG "THP")

1. Network interface configuration
![i1](png/p_interfaces1.PNG "i1")
![i2](png/p_interfaces2.PNG "i2")
![i3](png/p_interfaces3.PNG "i3")

1. Forward and reverse host lookups
* forward
![fw](png/p_getent.PNG "fw")
* reverse
![rev](png/p_getent2.PNG "rev")

1. nscd service running
![nscd](png/p_nscd.PNG "nscd")

1. ntpd service running
![ntpd](png/p_ntpd.PNG "ntpd")
