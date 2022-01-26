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

####uname command
 Displays  Linux system information
```sh
uname
```
Output:
```sh
Linux
```