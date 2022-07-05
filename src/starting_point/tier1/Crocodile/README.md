# Crocodile
## task 1
```
nmap -sC
```
## task 2
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# nmap -sV -p-1000 -T4 -sC 10.129.238.65
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-05 16:47 UTC
Nmap scan report for 10.129.238.65
Host is up (0.18s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.3
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
| -rw-r--r--    1 ftp      ftp            33 Jun 08  2021 allowed.userlist
|_-rw-r--r--    1 ftp      ftp            62 Apr 20  2021 allowed.userlist.passwd
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:10.10.14.193
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 3
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
80/tcp open  http    Apache httpd 2.4.41 ((Ubuntu))
|_http-title: Smash - Bootstrap Business Template
|_http-server-header: Apache/2.4.41 (Ubuntu)
Service Info: OS: Unix

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 20.64 seconds
```
vsftpd 3.0.3
## task 3
230
## task 4
get
## task 5
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# ftp <your target ip>
Connected to <your target ip>.
220 (vsFTPd 3.0.3)
Name (<your target ip>:root): Anonymous
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
229 Entering Extended Passive Mode (|||48811|)
150 Here comes the directory listing.
-rw-r--r--    1 ftp      ftp            33 Jun 08  2021 allowed.userlist
-rw-r--r--    1 ftp      ftp            62 Apr 20  2021 allowed.userlist.passwd
226 Directory send OK.
ftp> get allowed.userlist
local: allowed.userlist remote: allowed.userlist
229 Entering Extended Passive Mode (|||48726|)
150 Opening BINARY mode data connection for allowed.userlist (33 bytes).
100% |***************************************************************************************************************|    33       14.91 KiB/s    00:00 ETA
226 Transfer complete.
33 bytes received in 00:00 (0.18 KiB/s)
ftp> get allowed.userlist.passwd
local: allowed.userlist.passwd remote: allowed.userlist.passwd
229 Entering Extended Passive Mode (|||44447|)
150 Opening BINARY mode data connection for allowed.userlist.passwd (62 bytes).
100% |***************************************************************************************************************|    62      291.08 KiB/s    00:00 ETA
226 Transfer complete.
62 bytes received in 00:00 (0.34 KiB/s)
```
admin
## task 6
2.4.41
## task 7
Wappalyzer
## task 8
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# gobuster dir --help
```
```
gobuster dir -u <your target ip> -x <file extension>
```
## task 9
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# gobuster dir -u <your target ip> -w /usr/share/wordlists/dirb/common.txt -x php
===============================================================
Gobuster v3.1.0
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://<your target ip>
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.1.0
[+] Extensions:              php
[+] Timeout:                 10s
===============================================================
2022/07/05 16:58:41 Starting gobuster in directory enumeration mode
===============================================================
/.hta                 (Status: 403) [Size: 278]
/.hta.php             (Status: 403) [Size: 278]
/.htaccess            (Status: 403) [Size: 278]
/.htpasswd            (Status: 403) [Size: 278]
/.htaccess.php        (Status: 403) [Size: 278]
/.htpasswd.php        (Status: 403) [Size: 278]
/assets               (Status: 301) [Size: 315] [--> http://<your target ip>/assets/]
/config.php           (Status: 200) [Size: 0]
/css                  (Status: 301) [Size: 312] [--> http://<your target ip>/css/]
/dashboard            (Status: 301) [Size: 318] [--> http://<your target ip>/dashboard/]
/fonts                (Status: 301) [Size: 314] [--> http://<your target ip>/fonts/]
/index.html           (Status: 200) [Size: 58565]
/js                   (Status: 301) [Size: 311] [--> http://<your target ip>/js/]
/login.php            (Status: 200) [Size: 1577]
/logout.php           (Status: 302) [Size: 0] [--> login.php]
```
login.php
## Submit Flag