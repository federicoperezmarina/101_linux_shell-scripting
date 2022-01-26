# 101_linux_shell-scripting
This is a repository to learn how to use linux commands in shell &amp; how to create shell scripting

## Table of Contents

* [Linux Commands](#linux-commands)
* [Linux Shell Scripts](#linux-shell-scripts)

## Linux Commands
In this section we are going to learn commands to use in the linux shell. First of all we are going to start some docker images with linux SO.

```sh
#list docker images
docker images

#get ubuntu image
docker pull ubuntu:latest

#access into ubuntu
docker run -ti ubuntu /bin/bash
```
Groups of commands:
* [System commands](#system-commands)
* [Hardware commands](#hardware-commands)
* [Users commands](#users-commands)
* [File commands](#file-commands)

### System commands
Now we are going to learn some commands of linux system

* [uname](#uname)
* [uname -r](#uname--r)
* [uptime](#uptime)
* [hostname](#hostname)
* [hostname -i](#hostname--i)
* [date](#date)
* [whoami](#whoami)

#### uname
Displays  Linux system information
```sh
$ uname
Linux
```

#### uname -r
Displays  kernel release information
```sh
$ uname -r
5.10.47-linuxkit
```

#### uptime
Displays how long the system has been running including load average
```sh
$ uptime
01:36:49 up  8:07,  0 users,  load average: 0.10, 0.04, 0.01
```

#### hostname
Shows the system hostname
```sh
$ hostname
e2d78eff6e96
```

#### hostname -i
Displays the IP address of the system
```sh
$ hostname
e2d78eff6e96
```

#### date
Displays current system date and time
```sh
$ date
Wed Jan 26 01:37:05 UTC 2022
```

#### whoami
Displays who you are logged in as
```sh
$ whoami
root
```

### Hardware commands

* [cat /proc/cpuinfo](#cat--proc--cpuinfo)
* [cat /proc/meminfo](#cat--proc--meminfo)
* [lsblk](#lsblk)
* [free -m](#free--m)

#### cat /proc/cpuinfo
Displays more information about CPU e.g model, model name, cores, vendor id
```sh
$ cat /proc/cpuinfo
```

#### cat /proc/meminfo
Displays more information about CPU e.g model, model name, cores, vendor id
```sh
$ cat /proc/meminfo
```

#### lsblk
Displays block devices related information
```sh
$ lsblk
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
vda    254:0    0 59.6G  0 disk 
`-vda1 254:1    0 59.6G  0 part /etc/hosts
```

#### free -m
Displays free and used memory in the system (-m flag indicates memory in MB)
```sh
$ free -m
              total        used        free      shared  buff/cache   available
Mem:           1985         211        1156         343         617        1291
Swap:          1023           0        1023
```

### Users commands

* [id](#id)
* [last](#last)
* [groupadd "admin"](#groupadd--admin-)
* [adduser "nameuser"](#adduser--nameuser-)
* [userdel "nameuser"](#userdel--nameuser-)
* [usermod](#usermod)

#### id
Displays the details of the active user e.g. uid, gid, and groups
```sh
$ id
uid=0(root) gid=0(root) groups=0(root)
```

#### last
Shows the last logins in the system
```sh
$ last
wtmp begins Mon Jan 17 15:20:01 2022
```

#### groupadd "admin"
Adds the group 'admin'
```sh
$ cat /etc/group 
$ groupadd "admin"
$ cat /etc/group
```

#### adduser "nameuser"
add user Sam
```sh
$ cat /etc/passwd
$ adduser "Sam"
$ cat /etc/passwd
```

#### userdel "nameuser"
Deletes user Sam
```sh
$ cat /etc/passwd
$ userdel "Sam"
$ cat /etc/passwd
```

#### usermod
Used for changing / modifying user information
```sh
$ usermod
```

### File commands

* [ls](#ls)
* [pwd](#pwd)
* [mkdir](#mkdir)
* [rm](#rm)
* [cp](#cp)
* [mv](#mv)
* [touch](#touch) 
* [more](#more)
* [head](#head)
* [tail](#tail)
* [wc](#wc)

#### ls
Lists files - both regular &  hidden files and their permissions as well.
```sh
$ ls
```

#### pwd
Displays the current directory file path
```sh
$ pwd 
/tmp
```

#### mkdir
Creates a new directory
```sh
$ mkdir
```

#### rm
Removes files or directories
```sh
$ rm filename
$ rm -f filename
$ rm -r directory_name
$ rm -rf directory_name
```

#### cp
Copies files or directories
```sh
$ cp file1 file2
$ cp -r dir1 dir2
```

#### mv
Renames file1 to file2
```sh
$ mv file1 file2
```

#### touch
Creates a new file
```sh
$ touch filename
```

#### more
Outputs the contents of a file
```sh
$ more filename
```

#### head
Displays the first 10 lines of a file
```sh
$ head filename
```

#### tail
Displays the last 10 lines of a file
```sh
$ tail filename
```

#### wc
Prints the number of bytes, words and lines in a file
```sh
$ wc filename
```