# COMPLECS: Data Storage and Filesystems

Login to Expanse.

```
mkandes@hardtack:~$ ssh exp
Welcome to Bright release         9.0

                                                         Based on Rocky Linux 8
                                                                    ID: #000002

--------------------------------------------------------------------------------

                                 WELCOME TO
                  _______  __ ____  ___    _   _______ ______
                 / ____/ |/ // __ \/   |  / | / / ___// ____/
                / __/  |   // /_/ / /| | /  |/ /\__ \/ __/
               / /___ /   |/ ____/ ___ |/ /|  /___/ / /___
              /_____//_/|_/_/   /_/  |_/_/ |_//____/_____/

--------------------------------------------------------------------------------

Use the following commands to adjust your environment:

'module avail'            - show available modules
'module add <module>'     - adds a module to your environment for this session
'module initadd <module>' - configure module to be loaded at every login

-------------------------------------------------------------------------------
Last login: Tue Jul 29 09:46:37 2025 from 136.26.86.69
[etrain110@login01 ~]$
```

`cd` to `/` root directory of the login node and look around with `ls`.

```
[etrain110@login01 ~]$ cd /
[etrain110@login01 /]$ ls -lahtr
total 228K
drwxr-xr-x    2 root root 4.0K Nov 15  2019 tftpboot
drwxr-xr-x    2 root root 4.0K Oct 10  2021 srv
drwxr-xr-x    2 root root 4.0K Oct 10  2021 media
-rw-r--r--    1 root root    0 May 19  2022 .autorelabel
lrwxrwxrwx    1 root root    8 Apr  5  2023 sbin -> usr/sbin
lrwxrwxrwx    1 root root    9 Apr  5  2023 lib64 -> usr/lib64
lrwxrwxrwx    1 root root    7 Apr  5  2023 lib -> usr/lib
lrwxrwxrwx    1 root root    7 Apr  5  2023 bin -> usr/bin
drwxr-xr-x   13 root root 4.0K Apr  7  2023 usr
drwxr-xr-x    2 root root 4.0K Jun  8  2023 mnt
drwxr-xr-x    6 root root 4.0K Sep 21  2023 cm
drwxr-xr-x    7 root root 4.0K May  3  2024 opt
dr-xr-xr-x    5 root root 4.0K Jul  1  2024 boot
dr-xr-xr-x 3315 root root    0 Jun 18 07:20 proc
dr-xr-xr-x   13 root root    0 Jun 18 07:20 sys
drwx------    2 root root  16K Jun 18 07:27 lost+found
-rw-r--r--    1 root root  24K Jun 18 07:28 aquota.user
-rw-r--r--    1 root root  21K Jun 18 07:28 aquota.grp
dr-xr-xr-x   23 root root 4.0K Jun 18 07:28 ..
dr-xr-xr-x   23 root root 4.0K Jun 18 07:28 .
drwxr-xr-x    3 root root 4.0K Jun 18 07:28 scratch
drwxr-xr-x   24 root root 4.0K Jun 18 07:29 var
drwxr-xr-x  147 root root  12K Jun 18 07:30 etc
drwxr-xr-x   21 root root 5.0K Jul  6 07:37 dev
dr-xr-x---    6 root root 4.0K Jul 21 17:15 root
drwxr-xr-x    8 root root 4.0K Jul 25 06:01 expanse
drwxr-xr-x    3 root root    0 Aug  3 07:44 cvmfs
drwxr-xr-x 4449 root root    0 Aug  3 13:30 home
drwxrwxrwt  335 root root  92K Aug  3 13:33 tmp
drwxr-xr-x   38 root root 1.3K Aug  3 13:33 run
[etrain110@login01 /]$
```

Use the `tree` command to get a different view of the file system hierarchy.

```
[etrain110@login01 /]$ tree -L 1 -d
.
├── bin -> usr/bin
├── boot
├── cm
├── cvmfs
├── dev
├── etc
├── expanse
├── home
├── lib -> usr/lib
├── lib64 -> usr/lib64
├── lost+found
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin -> usr/sbin
├── scratch
├── srv
├── sys
├── tftpboot
├── tmp
├── usr
└── var

25 directories
[etrain110@login01 /]$
```

`cd` to `$HOME` and look around with `ls`.

```
[etrain110@login01 /]$ echo $HOME
/home/etrain110
[etrain110@login01 /]$ cd $HOME
[etrain110@login01 ~]$ ls -lahtr
total 93K
-rw-r--r--    1 etrain110 gue998  141 Aug  2  2022 .bash_profile
-rw-r--r--    1 etrain110 gue998   18 Aug  2  2022 .bash_logout
-rw-r--r--    1 etrain110 gue998  658 Sep 29  2022 .zshrc
-rw-r--r--    1 etrain110 gue998  334 Apr 12  2023 .emacs
-rw-r--r--    1 etrain110 gue998  172 Aug 25  2023 .kshrc
-rw-r--r--    1 etrain110 gue998    6 Jun 26 15:36 .ollama_port
-rw-------    1 etrain110 gue998  106 Jun 30 11:46 .Xauthority
-rw-------    1 etrain110 gue998 8.3K Jun 30 12:59 .viminfo
drwxr-xr-x    5 etrain110 gue998    5 Jul 28 18:52 .galyleo
-rw-r--r--    1 etrain110 gue998 2.7K Jul 28 19:04 .bashrc
lrwxrwxrwx    1 etrain110 gue998   34 Jul 28 19:17 data -> /cm/shared/examples/sdsc/ciml/2025
drwxr-x---    5 etrain110 gue998   16 Jul 29 09:28 .
drwxr-xr-x    3 etrain110 gue998    3 Jul 29 09:28 .ood_portal
drwx------    2 etrain110 gue998    4 Jul 29 09:45 .ssh
-rw-------    1 etrain110 gue998  15K Jul 29 09:53 .bash_history
drwxr-xr-x 4449 root      root      0 Aug  3 13:30 ..
[etrain110@login01 ~]$
```

Use the `df` command to look at the different filesystems available on Expanse. We'll truncate the output with the `head` command.

```
[etrain110@login01 ~]$ df -Th | head -n 20
Filesystem                                              Type      Size  Used Avail Use% Mounted on
devtmpfs                                                devtmpfs   63G     0   63G   0% /dev
tmpfs                                                   tmpfs      63G  7.7M   63G   1% /run
/dev/sda2                                               ext4       32G   24G  6.5G  79% /
tmpfs                                                   tmpfs      63G   90M   63G   1% /dev/shm
tmpfs                                                   tmpfs      63G     0   63G   0% /sys/fs/cgroup
/dev/sda4                                               ext4       32G  3.7G   26G  13% /tmp
/dev/sda1                                               vfat      100M     0  100M   0% /boot/efi
/dev/sdb1                                               ext4      879G   44K  834G   1% /scratch
10.22.100.111:/pool1/home                               nfs       213T   25T  189T  12% /expanse/nfs/home1
master:/home                                            nfs       140G   87G   54G  63% /expanse/nfs/mgr1/home
ps-071.sdsc.edu:/ps-data/community-sw                   nfs       1.0T  324G  701G  32% /expanse/community
10.22.101.201:/cw3e                                     nfs       171T  1.0M  171T   1% /expanse/nfs/cw3e
10.22.100.114:/pool4/home                               nfs       210T   26T  184T  13% /expanse/nfs/home4
10.22.100.113:/pool3/home                               nfs       201T   27T  175T  14% /expanse/nfs/home3
10.22.100.112:/pool2/home                               nfs       211T   31T  181T  15% /expanse/nfs/home2
10.21.0.21:6789,10.21.11.7:6789,10.21.11.8:6789:/       ceph      1.6T  1.3T  359G  78% /cm/shared
10.22.101.123@o2ib:10.22.101.124@o2ib:/expanse/scratch  lustre     11P  9.9P  975T  92% /expanse/lustre/scratch
tmpfs                                                   tmpfs      13G     0   13G   0% /run/user/0
10.22.100.114:/pool4/home/lddmm                         nfs       210T   26T  184T  13% /home/lddmm
[etrain110@login01 ~]$
```

Again, make sure you're in your $HOME directory, then check your current disk usage with the `du` command.

```
[etrain110@login01 ~]$ cd ~/
[etrain110@login01 ~]$ ls -lahtr
total 93K
-rw-r--r--    1 etrain110 gue998  141 Aug  2  2022 .bash_profile
-rw-r--r--    1 etrain110 gue998   18 Aug  2  2022 .bash_logout
-rw-r--r--    1 etrain110 gue998  658 Sep 29  2022 .zshrc
-rw-r--r--    1 etrain110 gue998  334 Apr 12  2023 .emacs
-rw-r--r--    1 etrain110 gue998  172 Aug 25  2023 .kshrc
-rw-r--r--    1 etrain110 gue998    6 Jun 26 15:36 .ollama_port
-rw-------    1 etrain110 gue998  106 Jun 30 11:46 .Xauthority
-rw-------    1 etrain110 gue998 8.3K Jun 30 12:59 .viminfo
drwxr-xr-x    5 etrain110 gue998    5 Jul 28 18:52 .galyleo
-rw-r--r--    1 etrain110 gue998 2.7K Jul 28 19:04 .bashrc
lrwxrwxrwx    1 etrain110 gue998   34 Jul 28 19:17 data -> /cm/shared/examples/sdsc/ciml/2025
drwxr-x---    5 etrain110 gue998   16 Jul 29 09:28 .
drwxr-xr-x    3 etrain110 gue998    3 Jul 29 09:28 .ood_portal
drwx------    2 etrain110 gue998    4 Jul 29 09:45 .ssh
-rw-------    1 etrain110 gue998  15K Jul 29 09:53 .bash_history
drwxr-xr-x 4449 root      root      0 Aug  3 13:30 ..
[etrain110@login01 ~]$ du -h $HOME
19K	/home/etrain110/.ssh
4.0G	/home/etrain110/.galyleo/py-light
185M	/home/etrain110/.galyleo/llm
806M	/home/etrain110/.galyleo/pyspark
5.0G	/home/etrain110/.galyleo
512	/home/etrain110/.ood_portal/batch_connect/cache
1.0K	/home/etrain110/.ood_portal/batch_connect
1.5K	/home/etrain110/.ood_portal
5.0G	/home/etrain110
[etrain110@login01 ~]$
```

Check how much memory is available on the login node.

```
[etrain110@login01 ~]$ free -h
              total        used        free      shared  buff/cache   available
Mem:          124Gi        59Gi        12Gi       124Mi        52Gi        63Gi
Swap:          11Gi       9.5Gi       2.5Gi
[etrain110@login01 ~]$
```
