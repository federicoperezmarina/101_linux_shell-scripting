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

### System
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
