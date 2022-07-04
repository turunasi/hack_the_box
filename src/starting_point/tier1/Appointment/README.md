# Appointment
## task 1
Structured Query Language
## task 2
SQL Injection
## task 3
Personally Identifiable Information
## task 4
@see https://owasp.org/www-project-top-ten/
A03:2021-Injection
## task 5
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# nmap -sV -T4 -F <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-04 05:43 UTC
Nmap scan report for <your target ip>
Host is up (0.21s latency).
Not shown: 99 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.38 ((Debian))

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.43 seconds
```
Apache httpd 2.4.38 ((Debian))
## task 6
443
## task 7
brute-forcing
## task 8
directory
## task 9
404
## task 10
```
gobuster dir -u <your target ip> -w <wordlist path>
```
## task 11
access <your target ip> and login
username : admin'#
password : <arbitrary password>