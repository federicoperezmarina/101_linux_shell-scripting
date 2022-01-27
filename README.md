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
### Groups of commands:
* [System commands](#system-commands)
* [Hardware commands](#hardware-commands)
* [Users commands](#users-commands)
* [File commands](#file-commands)
* [Process commands](#process-commands)
* [File permission commands](#file-permission-commands)
* [Network commands](#network-commands)
* [Compression/Archives commands](#compressionarchives-commands)
* [Search commands](#search-commands)
* [Disk usage commands](#disk-usage-commands)
* [File transfer commands](#file-transfer-commands)


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

### Process commands

* [ps](#ps)
* [top](#top)
* [kill](#kill)

#### ps
Display currently active processes
```sh
$ ps
  PID TTY          TIME CMD
    1 pts/0    00:00:00 bash
   97 pts/0    00:00:00 ps
```

#### top
Displays all running processes
```sh
$ top
```

#### kill
Terminates process with a given pid
```sh
$ kill pid
```

### File permission commands

* [chmod](#chmod)
* [chown](#chown)

#### chmod
Change file permissions
```sh
$ chmod octal filename
$ chmod 777 filename
```

#### chown
Change ownership of the file
```sh
$ chown owner filename
```

### Network commands

* [ifconfig ](#ifconfig)
* [ping](#ping)
* [whois](#whois)
* [dig](#dig)
* [host](#host)
* [wget](#wget)
* [netstat](#netstat)

#### ifconfig 
Displays IP addresses of all network interfaces
```sh
$ ifconfig
```

#### ping 
ping command sends an ICMP echo request to establish a connection to server / PC
```sh
$ ping www.marca.com
```

#### whois
Retrieves more information about a domain name
```sh
$ whois marca.com
```

#### dig
Retrieves DNS information about the domain
```sh
$ dig marca.com
```

#### wget
Downloads a file from an online source
```sh
$ wget filename
```

#### netstat
Displays all active listening ports
```sh
$ netstat
```

### Compression/Archives commands

* [tar](#)
* [gzip](#gzip)

#### tar 
Creates, extract and gzip tar files
```sh
$ tar -cf home.tar home<:code>
$ tar -xf files.tar
$ tar -zcvf home.tar.gz source-folder
```

#### gzip 
Compression a file with .gz extension
```sh
$ gzip file
```

### Search commands

* [grep](#grep)
* [find](#gzip)

#### grep 
Search for a given pattern
```sh
$ grep 'pattern' files
$ grep -r pattern dir  
```

#### find 
Find file given some parameters
```sh
$ find /home/ -name "index" 
$ find /home -size +10000k
```

### Disk Usage commands

* [df](#df)
* [fdisk](#fdisk)
* [du](#du)
* [mount](#mount)

#### df 
Display free space on mounted systems & displays free inodes on filesystems
```sh
$ df -h
$ df -i  
```

#### fdisk 
Shows disk partitions, sizes, and types
```sh
$ fdisk -l
```

#### du 
Displays disk usage in the current directory in a human-readable 
```sh
$ du -sh
```

#### mount 
Mount a device
```sh
$ mount device-path mount-point
```

### File transfer commands

* [scp](#scp)
* [rsync](#rsync)

#### scp 
Securely copy file1.txt to server2 in /tmp directory
```sh
$ scp file1.txt server2/tmp  
```

#### rsync 
Synchronize contents in /home/apps directory with /backup  directory
```sh
$rsync -a /home/apps  /backup/ 
```