## Visiting the Website

Visiting the webpage gives the default apache page. Checking the source code also gives nothing but **robots.txt** exists:

![[Pasted image 20210815002258.png]]

Checking out **/sar2HTML**, we are prompted with a documentation page of **sar2HTML**

![[Pasted image 20210815002451.png]]

The page discloses the current version (v3.2.1). Checking if **searchsploit** does have exploits against this version:

![[Pasted image 20210815002608.png]]

And we do see we have two RCEs against the v3.2.1 version.
By using the python exploit, we can successfully execute code:

![[Pasted image 20210815002851.png]]

Knowing that we can execute commands, we should confirm that the target machine can reach out to our attacker machine:

1) Setup tcpdump to listen to icmp pings:
>![[Pasted image 20210815003100.png]]

2) Ping our attacker machine using the target machine
>![[Pasted image 20210815003155.png]]

And indeed, the two machines can talk
![[Pasted image 20210815003541.png]]

---

## FOOTHOLD

I tried executing a reverse shell using bash and netcat commands but it did not work so what I did was setup a web server with a php reverse shell and using **wget** from the target machine to download the file

![[Pasted image 20210815003959.png]]

![[Pasted image 20210815004046.png]]

Setup a netcat listener and visit the downloaded php reverse shell and we should get a shell:

![[Pasted image 20210815004251.png]]

---

## INTERNAL ENUMERATION

Checking the home directory of the user **love**, we only have **user.txt**:

![[Pasted image 20210815005215.png]]

Looking at the /var/www/html, we have a few files:

![[Pasted image 20210815004511.png]]

Reading **finally.sh**, we can see that it executes the file **write.sh**
![[Pasted image 20210815004722.png]]

While reading **write.sh**, we can see that it just makes a temporary file called gateway to the /tmp directory.

Looking at the permissions of **finally.sh**, it is owned by root.
Looking at the contents of the both files, it gave me an idea that a a **cronjob** might be running. Having this suspicion, I ran **pspy** to check the processes running on the machine:

![[Pasted image 20210815005846.png]]

and indeed, we do have a cronjob involving the two files.

---

## PRIVILEGE ESCALATION

Since we own the **write.sh** even though it is being run by **finally.sh** that is owned by root, we can edit it to reach back to us as root:

![[Pasted image 20210815010227.png]]

And setup a netcat listener on our attacker machine. Wait a few mins and we should get a connection back as root:

![[Pasted image 20210815011524.png]]

Reading the root.txt

![[Pasted image 20210815011542.png]]

# ROOTED

---