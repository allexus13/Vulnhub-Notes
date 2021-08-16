## ALL TCP PORTS

![[Pasted image 20210817005624.png]]

```bash
# Nmap 7.91 scan initiated Tue Aug 17 00:51:40 2021 as: nmap -p- -oN nmap/all-tcp -vv 192.168.0.103
Nmap scan report for 192.168.0.103
Host is up, received arp-response (0.63s latency).
Scanned at 2021-08-17 00:51:40 PST for 139s
Not shown: 65532 closed ports
Reason: 65532 resets
PORT   STATE SERVICE REASON
21/tcp open  ftp     syn-ack ttl 64
22/tcp open  ssh     syn-ack ttl 64
80/tcp open  http    syn-ack ttl 64
MAC Address: 08:00:27:FF:F0:62 (Oracle VirtualBox virtual NIC)

Read data files from: /usr/bin/../share/nmap
# Nmap done at Tue Aug 17 00:53:59 2021 -- 1 IP address (1 host up) scanned in 139.63 seconds
```

---

## OPEN PORTS ENUMERATED

### FTP (Anonymous Login Enabled) - 

![[Pasted image 20210817010041.png]]

### SSH (Ubuntu Focal) -
https://launchpad.net/ubuntu/+source/openssh/1:8.2p1-4ubuntu0.2

![[Pasted image 20210817010215.png]]

### HTTP

![[Pasted image 20210817010414.png]]

```bash
# Nmap 7.91 scan initiated Tue Aug 17 00:51:08 2021 as: nmap -sC -sV -oN nmap/1k-tcp -vv 192.168.0.103
Nmap scan report for 192.168.0.103
Host is up, received arp-response (0.16s latency).
Scanned at 2021-08-17 00:51:08 PST for 9s
Not shown: 997 closed ports
Reason: 997 resets
PORT   STATE SERVICE REASON         VERSION
21/tcp open  ftp     syn-ack ttl 64 vsftpd 3.0.3
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_-rw-r--r--    1 0        0             110 Jul 02 09:33 note.txt
| ftp-syst: 
|   STAT: 
| FTP server status:
|      Connected to ::ffff:192.168.0.102
|      Logged in as ftp
|      TYPE: ASCII
|      No session bandwidth limit
|      Session timeout in seconds is 300
|      Control connection is plain text
|      Data connections will be plain text
|      At session startup, client count was 3
|      vsFTPd 3.0.3 - secure, fast, stable
|_End of status
22/tcp open  ssh     syn-ack ttl 64 OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 ac:d2:7b:75:80:67:f2:9d:95:67:52:99:c8:2f:ab:7b (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCik2EU7iX6gl/QBn/2aSR5HvrCkz2++1iTwrppF4n8pokPcDH4z1flxZrk4nlJDWS18xMj9NZl8r/rjhoPNHMAHZemSKusLL6ksge95ANMDM373+nTFqMTRwEmab/AfYmJD+NH5GfhJlNDsJ1vamANzZASlYb65de9XG5rR/mGlMtZkidkTZdIONwPORaX+21hvXGgiU7XO7gLxAJstwlzhd4eQfPq+k/YlBrj+8yQOHm/qr+8dpuDvfXGXfPV8IeXhSivruVA/WS10KGwEVRFvkFwxxR4HmL4E1VqJAjlKI6zjgkt5azIHQ2h6wgq6bELEyqG5+deKZG2noF/IwIIqTZVrBU3bKf6EgArM7ySFFg0WFjdM94Onrzx86Jvdv8kiN4/cm9XtM0uib1k0d/RyFUAEtrzyH/2XBPVz4WoSAGMvXpYIwzCBqhz2RG1SKdunUfBy5qNzyGvHZB3awd+masOeZPpafCakhuP0fL++wXhN6nvIk4RO7f4I13GWW8=
|   256 78:ca:86:73:b6:87:06:08:eb:7a:9c:ab:cf:9d:89:16 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBMt5dPZZ+riN/MXoP1akXkWa8CgGJdeTM3LIVdEpikHl5a2A06m4jLLF9v+UJEb6o5YnxGHSHoJnPXkKDkrexRY=
|   256 93:49:d7:8c:1c:07:7e:8e:79:91:2b:bf:2d:0d:34:6b (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIOT8TtDtWdCXc8TK10X4W7o5FjlJOLDGF/c6EObaCg8P
80/tcp open  http    syn-ack ttl 64 Apache httpd 2.4.41 ((Ubuntu))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: Apache2 Ubuntu Default Page: It works
MAC Address: 08:00:27:FF:F0:62 (Oracle VirtualBox virtual NIC)
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Tue Aug 17 00:51:17 2021 -- 1 IP address (1 host up) scanned in 9.60 seconds
```

