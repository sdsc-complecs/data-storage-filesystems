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
