##### 1. 系统信息
➢`arch`：`显示机器的处理器架构`
```py
thanlon@thanlon-master:~$ arch
x86_64
```
➢`uname -m`：`显示机器的处理器架构`
```py
thanlon@thanlon-master:~$ uname -m
x86_64
```
➢`uname -r`：`显示正在使用的内核版本`
```py
thanlon@thanlon-master:~$ uname -r
5.3.0-25-generic
```
➢`dmidecode -q`：`显示硬件系统部件`
```js
root@thanlon-master:/home/thanlon# dmidecode -q
......
```
➢`cat /proc/cpuinfo`：`显示CPU信息`
```py
thanlon@thanlon-master:~$ cat /proc/cpuinfo
processor	: 0
vendor_id	: GenuineIntel
cpu family	: 6
model		: 142
model name	: Intel(R) Core(TM) i7-8565U CPU @ 1.80GHz
stepping	: 11
microcode	: 0xca
cpu MHz		: 1071.532
cache size	: 8192 KB
......
```
➢`cat /proc/interrupts`：`显示中断`
```py
thanlon@thanlon-master:~$ cat /proc/interrupts 
            CPU0       CPU1       CPU2       CPU3       CPU4       CPU5       CPU6       CPU7       
   0:          8          0          0          0          0          0          0          0  IR-IO-APIC    2-edge      timer
   1:          0          0          0          0          0          0          0      14440  IR-IO-APIC    1-edge      i8042
   8:          0          1          0          0          0          0          0          0  IR-IO-APIC    8-edge      rtc0
......
```
➢`cat /proc/meminfo`：`校验内存使用`
```py
thanlon@thanlon-master:~$ cat /proc/meminfo 
MemTotal:        8000024 kB
MemFree:         2730080 kB
MemAvailable:    4789432 kB
Buffers:          418460 kB
Cached:          2673968 kB
......
```
➢`cat /proc/swaps`：`显示哪些swap被使用`
```py
thanlon@thanlon-master:~$ cat /proc/swaps
Filename				Type		Size	Used	Priority
/dev/sda7                               partition	488444	0	-2
```
➢`cat /proc/version`：`显示内核的版本`
```js
Linux version 5.3.0-26-generic (buildd@lgw01-amd64-013) (gcc version 9.2.1 20191008 (Ubuntu 9.2.1-9ubuntu2)) #28-Ubuntu SMP Wed Dec 18 05:37:46 UTC 2019
```
➢`cat /proc/net/dev`：`显示网络适配器及统计`
```py
thanlon@thanlon-master:~$ cat /proc/net/dev
Inter-|   Receive                                                |  Transmit
 face |bytes    packets errs drop fifo frame compressed multicast|bytes    packets errs drop fifo colls carrier compressed
    lo:  248910    2471    0    0    0     0          0         0   248910    2471    0    0    0     0       0          0
  wlo1: 51694928   64462    0 2465    0     0          0         0 14169705   53551    0    0    0     0       0          0
```
➢`cat /proc/mounts`：`显示已加载的文件系统`
```py
sysfs /sys sysfs rw,nosuid,nodev,noexec,relatime 0 0
proc /proc proc rw,nosuid,nodev,noexec,relatime 0 0
udev /dev devtmpfs rw,nosuid,relatime,size=3972612k,nr_inodes=993153,mode=755 0 0
devpts /dev/pts devpts rw,nosuid,noexec,relatime,gid=5,mode=620,ptmxmode=000 0 0
tmpfs /run tmpfs rw,nosuid,noexec,relatime,size=800004k,mode=755 0 0
/dev/sda10 / ext4 rw,relatime,errors=remount-ro 0 0
/dev/sda11 /usr ext4 rw,relatime 0 0
securityfs /sys/kernel/security securityfs rw,nosuid,nodev,noexec,relatime 0 0
tmpfs /dev/shm tmpfs rw,nosuid,nodev 0 0
tmpfs /run/lock tmpfs rw,nosuid,nodev,noexec,relatime,size=5120k 0 0
tmpfs /sys/fs/cgroup tmpfs ro,nosuid,nodev,noexec,mode=755 0 0
cgroup2 /sys/fs/cgroup/unified cgroup2 rw,nosuid,nodev,noexec,relatime,nsdelegate 0 0
cgroup /sys/fs/cgroup/systemd cgroup rw,nosuid,nodev,noexec,relatime,xattr,name=systemd 0 0
pstore /sys/fs/pstore pstore rw,nosuid,nodev,noexec,relatime 0 0
efivarfs /sys/firmware/efi/efivars efivarfs rw,nosuid,nodev,noexec,relatime 0 0
bpf /sys/fs/bpf bpf rw,nosuid,nodev,noexec,relatime,mode=700 0 0
cgroup /sys/fs/cgroup/cpu,cpuacct cgroup rw,nosuid,nodev,noexec,relatime,cpu,cpuacct 0 0
cgroup /sys/fs/cgroup/freezer cgroup rw,nosuid,nodev,noexec,relatime,freezer 0 0
cgroup /sys/fs/cgroup/net_cls,net_prio cgroup rw,nosuid,nodev,noexec,relatime,net_cls,net_prio 0 0
cgroup /sys/fs/cgroup/memory cgroup rw,nosuid,nodev,noexec,relatime,memory 0 0
……
systemd-1 /proc/sys/fs/binfmt_misc autofs rw,relatime,fd=25,pgrp=1,timeout=0,minproto=5,maxproto=5,direct,pipe_ino=20670 0 0
hugetlbfs /dev/hugepages hugetlbfs rw,relatime,pagesize=2M 0 0
debugfs /sys/kernel/debug debugfs rw,nosuid,nodev,noexec,relatime 0 0
mqueue /dev/mqueue mqueue rw,nosuid,nodev,noexec,relatime 0 0
fusectl /sys/fs/fuse/connections fusectl rw,nosuid,nodev,noexec,relatime 0 0
configfs /sys/kernel/config configfs rw,nosuid,nodev,noexec,relatime 0 0
/dev/sda12 /var ext4 rw,relatime 0 0
/dev/sda15 /srv ext4 rw,relatime 0 0
/dev/sda14 /opt ext4 rw,relatime 0 0
/dev/sda13 /usr/local ext4 rw,relatime 0 0
/dev/sda8 /boot ext4 rw,relatime 0 0
/dev/sda1 /boot/efi vfat rw,relatime,fmask=0077,dmask=0077,codepage=437,iocharset=iso8859-1,shortname=mixed,errors=remount-ro 0 0
/dev/sda9 /home ext4 rw,relatime 0 0
/dev/sda16 /tmp ext4 rw,relatime 0 0
/dev/loop1 /snap/gnome-logs/81 squashfs ro,nodev,relatime 0 0
/dev/loop4 /snap/gtk-common-themes/1353 squashfs ro,nodev,relatime 0 0
/dev/loop2 /snap/sublime-text/85 squashfs ro,nodev,relatime 0 0
/dev/loop3 /snap/gtk-common-themes/1198 squashfs ro,nodev,relatime 0 0
/dev/loop6 /snap/gnome-3-28-1804/110 squashfs ro,nodev,relatime 0 0
/dev/loop5 /snap/gnome-calculator/536 squashfs ro,nodev,relatime 0 0
/dev/loop7 /snap/core/8213 squashfs ro,nodev,relatime 0 0
……
```
➢`lspci -tv`：`罗列PCI设备`
```py
thanlon@thanlon-master:~$ lspci -tv
-[0000:00]-+-00.0  Intel Corporation Device 3e34
           +-02.0  Intel Corporation UHD Graphics 620 (Whiskey Lake)
           +-04.0  Intel Corporation Xeon E3-1200 v5/E3-1500 v5/6th Gen Core Processor Thermal Subsystem
           +-08.0  Intel Corporation Xeon E3-1200 v5/v6 / E3-1500 v5 / 6th/7th Gen Core Processor Gaussian Mixture Model
           +-12.0  Intel Corporation Cannon Point-LP Thermal Controller
```
➢`lsusb -tv`：`显示USB设备`
```py
thanlon@thanlon-master:~$ lsusb -tv
/:  Bus 02.Port 1: Dev 1, Class=root_hub, Driver=xhci_hcd/6p, 10000M
    ID 1d6b:0003 Linux Foundation 3.0 root hub
/:  Bus 01.Port 1: Dev 1, Class=root_hub, Driver=xhci_hcd/12p, 480M
    ID 1d6b:0002 Linux Foundation 2.0 root hub
    |__ Port 3: Dev 2, If 0, Class=Human Interface Device, Driver=usbhid, 12M
        ID 25a7:fa61  
    |__ Port 3: Dev 2, If 1, Class=Human Interface Device, Driver=usbhid, 12M
        ID 25a7:fa61  
    |__ Port 6: Dev 3, If 0, Class=Video, Driver=uvcvideo, 480M
        ID 13d3:56c1 IMC Networks 
    |__ Port 6: Dev 3, If 1, Class=Video, Driver=uvcvideo, 480M
        ID 13d3:56c1 IMC Networks 
    |__ Port 8: Dev 4, If 1, Class=Wireless, Driver=btusb, 12M
        ID 13d3:3526 IMC Networks 
    |__ Port 8: Dev 4, If 0, Class=Wireless, Driver=btusb, 12M
        ID 13d3:3526 IMC Networks 
```
➢`date`：`显示系统日期`
```py
thanlon@thanlon-master:~$ date
2019年 12月 23日 星期一 16:00:58 CST
```
➢`cal 2019`：`显示2019年的日历表`
```py
                            2019
         一月                    二月                    三月           
日 一 二 三 四 五 六  日 一 二 三 四 五 六  日 一 二 三 四 五 六  
       1  2  3  4  5                  1  2                  1  2  
 6  7  8  9 10 11 12   3  4  5  6  7  8  9   3  4  5  6  7  8  9  
13 14 15 16 17 18 19  10 11 12 13 14 15 16  10 11 12 13 14 15 16  
20 21 22 23 24 25 26  17 18 19 20 21 22 23  17 18 19 20 21 22 23  
27 28 29 30 31        24 25 26 27 28        24 25 26 27 28 29 30  
                                            31                    

         四月                    五月                    六月           
日 一 二 三 四 五 六  日 一 二 三 四 五 六  日 一 二 三 四 五 六  
    1  2  3  4  5  6            1  2  3  4                     1  
 7  8  9 10 11 12 13   5  6  7  8  9 10 11   2  3  4  5  6  7  8  
14 15 16 17 18 19 20  12 13 14 15 16 17 18   9 10 11 12 13 14 15  
21 22 23 24 25 26 27  19 20 21 22 23 24 25  16 17 18 19 20 21 22  
28 29 30              26 27 28 29 30 31     23 24 25 26 27 28 29  
                                            30                    

         七月                    八月                    九月           
日 一 二 三 四 五 六  日 一 二 三 四 五 六  日 一 二 三 四 五 六  
    1  2  3  4  5  6               1  2  3   1  2  3  4  5  6  7  
 7  8  9 10 11 12 13   4  5  6  7  8  9 10   8  9 10 11 12 13 14  
14 15 16 17 18 19 20  11 12 13 14 15 16 17  15 16 17 18 19 20 21  
21 22 23 24 25 26 27  18 19 20 21 22 23 24  22 23 24 25 26 27 28  
28 29 30 31           25 26 27 28 29 30 31  29 30                 
                                                                  

         十月                   十一月                   十二月           
日 一 二 三 四 五 六  日 一 二 三 四 五 六  日 一 二 三 四 五 六  
       1  2  3  4  5                  1  2   1  2  3  4  5  6  7  
 6  7  8  9 10 11 12   3  4  5  6  7  8  9   8  9 10 11 12 13 14  
13 14 15 16 17 18 19  10 11 12 13 14 15 16  15 16 17 18 19 20 21  
20 21 22 23 24 25 26  17 18 19 20 21 22 23  22 23 24 25 26 27 28  
27 28 29 30 31        24 25 26 27 28 29 30  29 30 31  
```