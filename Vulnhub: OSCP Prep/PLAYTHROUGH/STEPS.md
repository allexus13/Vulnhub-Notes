# STEPS

## LOOKING THROUGH THE WEBSITE

Visiting the webpage, we are prompted with a **wordpress** blog. If we read the message, we will see that the author said that the only user in this box is **oscp**:

![[Pasted image 20210814234420.png]]

---

## FOOTHOLD

Using the SSH private key that we recovered before (refer to ATTACK VECTORS/Robots.txt), we should be able to log in with the user **oscp**

![[Pasted image 20210814234951.png]]

---

## PRIVILEGE ESCALATION

Checking the SUID binaries, we do have **/bin/bash**:

![[Pasted image 20210814235359.png]]

Using this, we scan spawn a root shell by using the command:

>/bin/bash -p

![[Pasted image 20210814235445.png]]

Reading the flag:

![[Pasted image 20210814235543.png]]

>flag.txt
d73b04b0e696b0945283defa3eee4538

# ROOTED!
---