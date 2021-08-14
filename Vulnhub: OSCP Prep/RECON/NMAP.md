## TOP 1k PORTS

![[Pasted image 20210814231346.png]]

```bash
# Nmap 7.91 scan initiated Sat Aug 14 23:10:59 2021 as: nmap -sC -sV -oN nmap/1k-tcp -vv 192.168.0.104
Nmap scan report for 192.168.0.104
Host is up, received arp-response (0.76s latency).
Scanned at 2021-08-14 23:11:00 PST for 16s
Not shown: 998 closed ports
Reason: 998 resets
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 64 OpenSSH 8.2p1 Ubuntu 4ubuntu0.1 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 91:ba:0d:d4:39:05:e3:13:55:57:8f:1b:46:90:db:e4 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDTlNTlvI4qQLNU17b70iKB5xuJlNnZ3zMZeHzfG3H5TcsVNmgImTe4FjEez0e4lKqJvTMsxrPVFHTq6gqfYHwN0KN34x0dv0ngrc+wrrWNoHQrQQqeFuTZy0Tt6BY97082YpFvZfDAvAwJoutkyCxeBb1+C9Y7g6kQYXlNFOuHoq/2m6vki9yVW7Bu3IVeLryw/7pnwzb/tr3K86GEsGc8+87ZIyFrgE1Rca/Y1hD03Uk0s/Kpmi3hCybJwPIoB1WmO2Xz2US8xqzuefsX6UzRazFTQKlTCq5gTTkpNE5fJzS/WmvK7w79aoFJPmVBCXOSXkoe9uoi9a64OnsY0jF8ao7uOUJp84QIUyPRLuPXqlxXwZenqt5RKH6dXyw9tsV2Q3BvZwJwvStFjiQFIi2zIp5jmVcYxwqV4CTt7Ev0ybATE00YAfCoS5i2LJR+fquN9XkS4ay3p9qoZZW7Q4uujWfUUaSO/gYLiOTpbTOl4Smgzc+NvqFrUk1OxPttDSc=
|   256 0f:35:d1:a1:31:f2:f6:aa:75:e8:17:01:e7:1e:d1:d5 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBOX6nl2HC2/Prh0l8uVsnAzinDT2+rhj1VasPM8Df3ntzgb8XzQat7zC/nHm0v7yLWo/CjpI6pD+mrBh3P/wuqk=
|   256 af:f1:53:ea:7b:4d:d7:fa:d8:de:0d:f2:28:fc:86:d7 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIBefJyPm1sjN+QedhTj6S1CPbXQZEFXb58RICJh970R8
80/tcp open  http    syn-ack ttl 64 Apache httpd 2.4.41 ((Ubuntu))
|_http-generator: WordPress 5.4.2
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
| http-robots.txt: 1 disallowed entry 
|_/secret.txt
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: OSCP Voucher &#8211; Just another WordPress site
MAC Address: 08:00:27:9A:38:2B (Oracle VirtualBox virtual NIC)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 14 23:11:16 2021 -- 1 IP address (1 host up) scanned in 17.47 seconds
```

---

## ALL TCP PORTS

![[Pasted image 20210814231609.png]]

```bash
# Nmap 7.91 scan initiated Sat Aug 14 23:11:32 2021 as: nmap -p- -oN nmap/all-tcp -vv 192.168.0.104
Nmap scan report for 192.168.0.104
Host is up, received arp-response (0.079s latency).
Scanned at 2021-08-14 23:11:32 PST for 202s
Not shown: 65532 closed ports
Reason: 65532 resets
PORT      STATE SERVICE REASON
22/tcp    open  ssh     syn-ack ttl 64
80/tcp    open  http    syn-ack ttl 64
33060/tcp open  mysqlx  syn-ack ttl 64
MAC Address: 08:00:27:9A:38:2B (Oracle VirtualBox virtual NIC)

Read data files from: /usr/bin/../share/nmap
# Nmap done at Sat Aug 14 23:14:54 2021 -- 1 IP address (1 host up) scanned in 202.47 seconds
```

---

## UNCOMMON PORTS

![[Pasted image 20210814232343.png]]

```bash
# Nmap 7.91 scan initiated Sat Aug 14 23:18:12 2021 as: nmap -p 33060 -sC -sV -oN nmap/uncommon-ports 192.168.0.104
Nmap scan report for 192.168.0.104
Host is up (0.00065s latency).

PORT      STATE SERVICE VERSION
33060/tcp open  mysqlx?
| fingerprint-strings: 
|   DNSStatusRequestTCP, LDAPSearchReq, NotesRPC, SSLSessionReq, TLSSessionReq, X11Probe, afp: 
|     Invalid message"
|_    HY000
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port33060-TCP:V=7.91%I=7%D=8/14%Time=6117DEBB%P=x86_64-pc-linux-gnu%r(N
SF:ULL,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(GenericLines,9,"\x05\0\0\0\x0b\
SF:x08\x05\x1a\0")%r(GetRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(HTTPOp
SF:tions,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(RTSPRequest,9,"\x05\0\0\0\x0b
SF:\x08\x05\x1a\0")%r(RPCCheck,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(DNSVers
SF:ionBindReqTCP,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(DNSStatusRequestTCP,2
SF:B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fI
SF:nvalid\x20message\"\x05HY000")%r(Help,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")
SF:%r(SSLSessionReq,2B,"\x05\0\0\0\x0b\x08\x05\x1a\0\x1e\0\0\0\x01\x08\x01
SF:\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000")%r(TerminalServerCookie
SF:,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(TLSSessionReq,2B,"\x05\0\0\0\x0b\x
SF:08\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"
SF:\x05HY000")%r(Kerberos,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(SMBProgNeg,9
SF:,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(X11Probe,2B,"\x05\0\0\0\x0b\x08\x05\
SF:x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY0
SF:00")%r(FourOhFourRequest,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LPDString,
SF:9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LDAPSearchReq,2B,"\x05\0\0\0\x0b\x0
SF:8\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\
SF:x05HY000")%r(LDAPBindReq,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(SIPOptions
SF:,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(LANDesk-RC,9,"\x05\0\0\0\x0b\x08\x
SF:05\x1a\0")%r(TerminalServer,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(NCP,9,"
SF:\x05\0\0\0\x0b\x08\x05\x1a\0")%r(NotesRPC,2B,"\x05\0\0\0\x0b\x08\x05\x1
SF:a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\x05HY000
SF:")%r(JavaRMI,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(WMSRequest,9,"\x05\0\0
SF:\0\x0b\x08\x05\x1a\0")%r(oracle-tns,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r
SF:(ms-sql-s,9,"\x05\0\0\0\x0b\x08\x05\x1a\0")%r(afp,2B,"\x05\0\0\0\x0b\x0
SF:8\x05\x1a\0\x1e\0\0\0\x01\x08\x01\x10\x88'\x1a\x0fInvalid\x20message\"\
SF:x05HY000")%r(giop,9,"\x05\0\0\0\x0b\x08\x05\x1a\0");
MAC Address: 08:00:27:9A:38:2B (Oracle VirtualBox virtual NIC)

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Aug 14 23:18:34 2021 -- 1 IP address (1 host up) scanned in 22.21 seconds
```

