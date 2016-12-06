#0. add disk
```
sudo fdisk /dev/xvdb
sudo mkfs.ext4 /dev/xvdb1
sudo mkfs.ext4 /dev/xvdb2

edit /etc/fstab
/dev/xvdb1      /opt    ext4    defaults,noatime        1       2
/dev/xvdb2      /data   ext4    defaults,noatime        1       2

sudo mount -a

df -a

Filesystem     1K-blocks    Used Available Use% Mounted on
/dev/xvda1       6061632 2918652   2828408  51% /
proc                   0       0         0    - /proc
sysfs                  0       0         0    - /sys
devpts                 0       0         0    - /dev/pts
tmpfs            7648804       0   7648804   0% /dev/shm
none                   0       0         0    - /proc/sys/fs/binfmt_misc
/dev/xvdb1      11775668   29544  11141280   1% /opt
/dev/xvdb2      18923424   44992  17910516   1% /data
```

show mount 
```
mount -v
[ec2-user@ip-172-31-7-44 /]$ sudo mount -v
/dev/xvda1 on / type ext4 (rw)
proc on /proc type proc (rw)
sysfs on /sys type sysfs (rw)
devpts on /dev/pts type devpts (rw,gid=5,mode=620)
tmpfs on /dev/shm type tmpfs (rw,rootcontext="system_u:object_r:tmpfs_t:s0")
none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
/dev/xvdb1 on /opt type ext4 (rw,noatime)
/dev/xvdb2 on /data type ext4 (rw,noatime)

 sudo tune2fs -l /dev/xvdb1
tune2fs 1.41.12 (17-May-2010)
Filesystem volume name:   <none>
Last mounted on:          <not available>
Filesystem UUID:          c041ed07-19a7-4e51-ae8c-f47034ccc9f1
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
Filesystem flags:         signed_directory_hash
Default mount options:    (none)
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              757392
Block count:              3024228
Reserved block count:     151211
Free blocks:              2936531
Free inodes:              757381
First block:              0
Block size:               4096
Fragment size:            4096
Reserved GDT blocks:      738
Blocks per group:         32768
Fragments per group:      32768
Inodes per group:         8144
Inode blocks per group:   509
Flex block group size:    16
Filesystem created:       Mon Dec  5 03:57:46 2016
Last mount time:          Mon Dec  5 04:14:47 2016
Last write time:          Mon Dec  5 04:14:47 2016
Mount count:              1
Maximum mount count:      20
Last checked:             Mon Dec  5 03:57:46 2016
Check interval:           15552000 (6 months)
Next check after:         Sat Jun  3 04:57:46 2017
Lifetime writes:          316 MB
Reserved blocks uid:      0 (user root)
Reserved blocks gid:      0 (group root)
First inode:              11
Inode size:               256
Required extra isize:     28
Desired extra isize:      28
Journal inode:            8
Default directory hash:   half_md4
Directory Hash Seed:      ff33c672-ba9e-4bd2-b845-ec07bc8ab2e4
Journal backup:           inode blocks

 sudo tune2fs -l /dev/xvdb2
tune2fs 1.41.12 (17-May-2010)
Filesystem volume name:   <none>
Last mounted on:          <not available>
Filesystem UUID:          a5f888a1-4a84-4819-9a3b-855309da0990
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
Filesystem flags:         signed_directory_hash
Default mount options:    (none)
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              1210048
Block count:              4839581
Reserved block count:     241979
Free blocks:              4719608
Free inodes:              1210037
First block:              0
Block size:               4096
Fragment size:            4096
Reserved GDT blocks:      1022
Blocks per group:         32768
Fragments per group:      32768
Inodes per group:         8176
Inode blocks per group:   511
Flex block group size:    16
Filesystem created:       Mon Dec  5 03:58:07 2016
Last mount time:          Mon Dec  5 04:14:47 2016
Last write time:          Mon Dec  5 04:14:47 2016
Mount count:              1
Maximum mount count:      22
Last checked:             Mon Dec  5 03:58:07 2016
Check interval:           15552000 (6 months)
Next check after:         Sat Jun  3 04:58:07 2017
Lifetime writes:          428 MB
Reserved blocks uid:      0 (user root)
Reserved blocks gid:      0 (group root)
First inode:              11
Inode size:               256
Required extra isize:     28
Desired extra isize:      28
Journal inode:            8
Default directory hash:   half_md4
Directory Hash Seed:      028cc135-0c6e-465b-92a0-be4d14e1a9d1
Journal backup:           inode blocks
```
reset reserve blockcount to 0
```
sudo tune2fs -m0 /dev/xvdb1

 sudo tune2fs -l /dev/xvdb1
tune2fs 1.41.12 (17-May-2010)
Filesystem volume name:   <none>
Last mounted on:          <not available>
Filesystem UUID:          c041ed07-19a7-4e51-ae8c-f47034ccc9f1
Filesystem magic number:  0xEF53
Filesystem revision #:    1 (dynamic)
Filesystem features:      has_journal ext_attr resize_inode dir_index filetype needs_recovery extent flex_bg sparse_super large_file huge_file uninit_bg dir_nlink extra_isize
Filesystem flags:         signed_directory_hash
Default mount options:    (none)
Filesystem state:         clean
Errors behavior:          Continue
Filesystem OS type:       Linux
Inode count:              757392
Block count:              3024228
Reserved block count:     0
```

#1. edit /etc/hosts
```
172.31.7.44 sit_cm
172.31.7.45 sit_d1
172.31.7.43 sit_d2
172.31.7.46 sit_d3
172.31.7.42 sit_rm
```
#2. edit /etc/ssh/sshd_config
PermitRootLogin yes
PasswordAuthentication yes
2.1 create root passwd
sudo passwd root
2.1 restart sshd service
sudo service sshd restart

#3. setup jdk
sudo yum install jdk-7u75-linux-x64.rpm

#4. setup mysql connector
sudo yum install mysql-connector-java

#5. set vm.swappiness
sudo sysctl vm.swappiness=1
sudo vi /etc/sysctl.conf 
vm.swappiness=1

#6. disable hugepage and add to /etc/rc.local
echo never > /sys/kernel/mm/redhat_transparent_hugepage/defrag

[ec2-user@ip-172-31-7-42 ~]$ sudo cat /sys/kernel/mm/transparent_hugepage/defrag
always madvise [never]

#7. (to disable add the following to /etc/sysctl.conf) 

disable ipv6 
```
net.ipv6.conf.all.disable_ipv6 = 1
net.ipv6.conf.default.disable_ipv6 = 1
net.ipv6.conf.lo.disable_ipv6 = 1  
```
adding below setting in /etc/sysconfig/network
```
NETWORKING_IPV6=no
NOZEROCONF=yes
IPV6INIT=no
```

#8.Show forward and reverse host lookups using getent and nslookup
```
[root@ip-172-31-7-44 ~]# getent hosts ip-172-31-7-44.ap-southeast-1.compute.internal
172.31.7.44     ip-172-31-7-44.ap-southeast-1.compute.internal
```

```
[root@ip-172-31-7-44 ~]# nslookup 172.31.7.44
Server:         172.31.0.2
Address:        172.31.0.2#53
```
Non-authoritative answer:
```
44.7.31.172.in-addr.arpa        name = ip-172-31-7-44.ap-southeast-1.compute.internal.
```
Authoritative answers can be found from:

#start nscd
```
sudo yum install nscd
sudo service nscd start && chkconfig nscd on

ps -ef | grep nscd
nscd     26081     1  0 05:21 ?        00:00:00 /usr/sbin/nscd
```
start ntpd
```
service ntpd start
```
##########################
disabled selinux
edit /etc/selinux/config
SELINUX=disabled



