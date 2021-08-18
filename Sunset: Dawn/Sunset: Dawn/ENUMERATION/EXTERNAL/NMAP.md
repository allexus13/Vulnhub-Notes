## TOP 1k PORTS

![[Pasted image 20210819013812.png]]

![[Pasted image 20210819013835.png]]

```bash
# Nmap 7.91 scan initiated Thu Aug 19 01:29:10 2021 as: nmap -sC -sV -oN nmap/1k-tcp -vv 192.168.0.103
Nmap scan report for 192.168.0.103
Host is up, received arp-response (0.72s latency).
Scanned at 2021-08-19 01:29:11 PST for 15s
Not shown: 996 closed ports
Reason: 996 resets
PORT     STATE SERVICE     REASON         VERSION
80/tcp   open  http        syn-ack ttl 64 Apache httpd 2.4.38 ((Debian))
| http-methods: 
|_  Supported Methods: GET POST OPTIONS HEAD
|_http-server-header: Apache/2.4.38 (Debian)
|_http-title: Site doesn't have a title (text/html).
139/tcp  open  netbios-ssn syn-ack ttl 64 Samba smbd 3.X - 4.X (workgroup: WORKGROUP)
445/tcp  open  netbios-ssn syn-ack ttl 64 Samba smbd 4.9.5-Debian (workgroup: WORKGROUP)
3306/tcp open  mysql       syn-ack ttl 64 MySQL 5.5.5-10.3.15-MariaDB-1
| mysql-info: 
|   Protocol: 10
|   Version: 5.5.5-10.3.15-MariaDB-1
|   Thread ID: 14
|   Capabilities flags: 63486
|   Some Capabilities: SupportsCompression, Speaks41ProtocolNew, LongColumnFlag, SupportsTransactions, IgnoreSpaceBeforeParenthesis, ODBCClient, Support41Auth, DontAllowDatabaseTableColumn, InteractiveClient, Speaks41ProtocolOld, IgnoreSigpipes, FoundRows, SupportsLoadDataLocal, ConnectWithDatabase, SupportsMultipleStatments, SupportsAuthPlugins, SupportsMultipleResults
|   Status: Autocommit
|   Salt: tct=qEBZ!2ux})SFFi`%
|_  Auth Plugin Name: mysql_native_password
MAC Address: 08:00:27:BE:44:3C (Oracle VirtualBox virtual NIC)
Service Info: Host: DAWN

Host script results:
|_clock-skew: mean: -6h39m56s, deviation: 2h18m33s, median: -7h59m56s
| nbstat: NetBIOS name: DAWN, NetBIOS user: <unknown>, NetBIOS MAC: <unknown> (unknown)
| Names:
|   DAWN<00>             Flags: <unique><active>
|   DAWN<03>             Flags: <unique><active>
|   DAWN<20>             Flags: <unique><active>
|   \x01\x02__MSBROWSE__\x02<01>  Flags: <group><active>
|   WORKGROUP<00>        Flags: <group><active>
|   WORKGROUP<1e>        Flags: <group><active>
| Statistics:
|   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
|   00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00
|_  00 00 00 00 00 00 00 00 00 00 00 00 00 00
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 62501/tcp): CLEAN (Couldn't connect)
|   Check 2 (port 62811/tcp): CLEAN (Couldn't connect)
|   Check 3 (port 42712/udp): CLEAN (Failed to receive data)
|   Check 4 (port 35829/udp): CLEAN (Failed to receive data)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked
| smb-os-discovery: 
|   OS: Windows 6.1 (Samba 4.9.5-Debian)
|   Computer name: dawn
|   NetBIOS computer name: DAWN\x00
|   Domain name: dawn
|   FQDN: dawn.dawn
|_  System time: 2021-08-18T05:29:30-04:00
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
| smb2-security-mode: 
|   2.02: 
|_    Message signing enabled but not required
| smb2-time: 
|   date: 2021-08-18T09:29:30
|_  start_date: N/A

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Thu Aug 19 01:29:26 2021 -- 1 IP address (1 host up) scanned in 16.26 seconds
```

---

## ALL TCP PORTS

![[Pasted image 20210819013903.png]]

```bash
# Nmap 7.91 scan initiated Thu Aug 19 01:31:55 2021 as: nmap -p- -oN nmap/all-tcp -vv 192.168.0.103
Nmap scan report for 192.168.0.103
Host is up, received arp-response (0.082s latency).
Scanned at 2021-08-19 01:31:55 PST for 203s
Not shown: 65531 closed ports
Reason: 65531 resets
PORT     STATE SERVICE      REASON
80/tcp   open  http         syn-ack ttl 64
139/tcp  open  netbios-ssn  syn-ack ttl 64
445/tcp  open  microsoft-ds syn-ack ttl 64
3306/tcp open  mysql        syn-ack ttl 64
MAC Address: 08:00:27:BE:44:3C (Oracle VirtualBox virtual NIC)

Read data files from: /usr/bin/../share/nmap
# Nmap done at Thu Aug 19 01:35:18 2021 -- 1 IP address (1 host up) scanned in 203.03 seconds
```