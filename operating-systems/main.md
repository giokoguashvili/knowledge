# Linux Networking
- [Linux Networking Commands with Examples](https://mindmajix.com/linux-networking-commands-best-examples)

## Commands
```
netstat/ss 
ifconfig/ip       
traceroute/tracepath
nslookup/dig
route
host
hostname
arp
iwconfig
tcpdump
ping
mtr (ping + traceroute)
curl/wget
whois
```

# Command-line
- **Terminal** <br/>
A terminal is a text input and output environment
- **Console** <br/>
A console is a physical terminal 
- **Shell** <br/>
is an interface between the user and the operating system
- **sh** <br/>
implements the shell interface, that actually processes commands and outputs results
- **bash** <br/>
is a superset of sh
- **Command-line** <br/>
A command-line interface (CLI) is a computer program that processes commands in the form of lines of text. The user typically interacts with the shell via a command-line interface (CLI).

# Directory Tree, File Systems & Files

- UFS - Universal Flash Storage
- NFS - Network File System
- CDFS - Compact Disc File System
- SMB - Server Message Block is a network protocol used for file transfer
- CIFS - Common Internet File System is a version of SMB introduced by Microsoft in 1996 with the release of Windows 95

![Directories](https://user-images.githubusercontent.com/8178412/208289340-c7b752a7-a18c-44e1-ae55-696f97ba4907.png)


- **File System** is a methodology for logically organizing and storing large quantities of data such that the system is easy to manage. a file system consists of files, relationships to other files, as well as the attributes(file type, file name, file size, file owner, file timestamp) of each file.

- **Directories:** for example, the Unix file system is essentially composed of files and directories. Directories are special files that may contain other files. the top-most directory is / (slash), with the directories directly beneath being system directories.

`/` - Root of Linux Filesystem <br/>
`/bin` - Binary Executable files are kept here <br/>
`/boot` - Booting related files are kept here <br/>
`/dev` - Device files are kept here <br/>
`/etc` - System-wide configuration files are kept here <br/>
`/home` - Location for the home directories of regular users <br/>
`/lib64` - Libraries for binary executables are kept here <br/>
`/mnt` - Temporary mount point for DVD-Rom, USB flash drive <br/>
`/opt` - Optional Programs are installed here like Program Files in Windows <br/>
`/proc` - Kernel pseudo filesystem <br/>
`/root` - Home directory of super user root <br/>
`/sbin` - System Binary Executable files are kept here <br/>
`/tmp` - Temporary files are kept here <br/>
`/usr` - User Filesystem <br/>
`/var` - Variable files are kept here <br/>
`/srv` - is a serve folder, contains site-specific data which is served by this system <br/>

# The following table lists the symbol of different types of files

| Character |   Meaning | Description |
| - |   - | - |
| `-` | Regular or ordinary file | Contain data of various content types such as text, script, image, videos, etc |
| `d` | Directory file | Contain the name and address of other files |
| `l` | Link file | Point or mirror other files |
| `b` | Block special file | Represent device files such as hard drives, monitors, etc |
| `p` | Named pipe file | Allow processes to send data to other processes or receive data from other processes |
| `c` | Character special file |
| `s` | Socket file | Provide inter-process communication |

# Commands

```
uname -a
w
id
whoami
lsmod
```

```
whoami
info
cal
lscpu
uptime
man
locate
whereis
ping
clear
pwd
ls -la

cat
more
less

touch
cp
mv
rm

ln

fee -h
dmesg

sudo su
last
who
w
id

useradd
passwd
userdel

groupadd
groupdel
sudo usermod -aG sudo <username>

/etc/passwd
/etc/shadow

file <filePath>

stat
lsof
```

# Gloassary

- **sda** - scsi disk