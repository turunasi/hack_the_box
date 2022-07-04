# Meow
## task 1
Virtual Machine
## task 2
Terminal
## task 3
OpenVPN
## task 4
tun
## task 5
ping
## task 6
nmap
## task 7
```
┌──(root㉿cbfc9d3c3a36)-[/mnt/src/starting_point]
└─# nmap <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-04 01:53 UTC
Nmap scan report for <your target ip>
Host is up (0.18s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE
23/tcp open  telnet

Nmap done: 1 IP address (1 host up) scanned in 1.78 seconds
```
telnet
## task 8
root
## task 9
```
┌──(root㉿cbfc9d3c3a36)-[/]
└─# telnet 10.129.164.245
Trying 10.129.164.245...
Connected to 10.129.164.245.
Escape character is '^]'.

  █  █         ▐▌     ▄█▄ █          ▄▄▄▄
  █▄▄█ ▀▀█ █▀▀ ▐▌▄▀    █  █▀█ █▀█    █▌▄█ ▄▀▀▄ ▀▄▀
  █  █ █▄█ █▄▄ ▐█▀▄    █  █ █ █▄▄    █▌▄█ ▀▄▄▀ █▀█


Meow login: root
Welcome to Ubuntu 20.04.2 LTS (GNU/Linux 5.4.0-77-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

  System information as of Mon 04 Jul 2022 02:02:41 AM UTC

  System load:           0.0
  Usage of /:            41.7% of 7.75GB
  Memory usage:          4%
  Swap usage:            0%
  Processes:             137
  Users logged in:       0
  IPv4 address for eth0: 10.129.164.245
  IPv6 address for eth0: dead:beef::250:56ff:feb9:88c6

 * Super-optimized for small spaces - read how we shrank the memory
   footprint of MicroK8s to make it the smallest full K8s around.

   https://ubuntu.com/blog/microk8s-memory-optimisation

75 updates can be applied immediately.
31 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable


The list of available updates is more than a week old.
To check for new updates run: sudo apt update

Last login: Mon Sep  6 15:15:23 UTC 2021 from 10.10.14.18 on pts/0
root@Meow:~# ls
flag.txt  snap
root@Meow:~# cat flag.txt
```