## TOP 1k PORTS

![[Pasted image 20210815001906.png]]

```bash
# Nmap 7.91 scan initiated Sun Aug 15 00:17:24 2021 as: nmap -sC -sV -oN nmap/1k-tcp -vv 192.168.0.105
Nmap scan report for 192.168.0.105
Host is up, received arp-response (0.61s latency).
Scanned at 2021-08-15 00:17:25 PST for 12s
Not shown: 999 closed ports
Reason: 999 resets
PORT   STATE SERVICE REASON         VERSION
80/tcp open  http    syn-ack ttl 64 Apache httpd 2.4.29 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Apache2 Ubuntu Default Page: It works
MAC Address: 08:00:27:AC:6F:4B (Oracle VirtualBox virtual NIC)

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sun Aug 15 00:17:37 2021 -- 1 IP address (1 host up) scanned in 13.68 seconds
```

---

## ALL TCP PORTS

![[Pasted image 20210815002220.png]]

```bash
# Nmap 7.91 scan initiated Sun Aug 15 00:17:51 2021 as: nmap -p- -oN nmap/all-tcp -vv 192.168.0.105
Nmap scan report for 192.168.0.105
Host is up, received arp-response (1.0s latency).
Scanned at 2021-08-15 00:17:51 PST for 213s
Not shown: 65534 closed ports
Reason: 65534 resets
PORT   STATE SERVICE REASON
80/tcp open  http    syn-ack ttl 64
MAC Address: 08:00:27:AC:6F:4B (Oracle VirtualBox virtual NIC)

Read data files from: /usr/bin/../share/nmap
# Nmap done at Sun Aug 15 00:21:24 2021 -- 1 IP address (1 host up) scanned in 212.94 seconds
```

