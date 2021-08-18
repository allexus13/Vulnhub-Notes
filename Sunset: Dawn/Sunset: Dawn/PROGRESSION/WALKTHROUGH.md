Visiting the webpage, we are greeted with a simple page. Using **GOBUSTER**, we found:

- **/logs**

Visiting **/logs**, we can find a bunch of files

![[Pasted image 20210819021450.png]]

All files aside from **management.log** are forbidden to download

Viewing **management.log**, it looks like a copy of the processes running on our target system. This was done using **pspy**

![[Pasted image 20210819021644.png]]

Reading through the log, we can see that there is a **cronjob** set to execute the **web-control** file located in the **ITDEPT** directory in the **smb** share. We can take advantage of this by uploading a bash reverse shell named **web-control**

![[Pasted image 20210819021811.png]]

After setting a netcat listener, we should be able to get a shell

![[Pasted image 20210819021939.png]]

After stabilizing our shell, we can check our **sudo** rules

![[Pasted image 20210819023439.png]]

Since we can run **sudo** as root, we can just easily spawn a shell as **root**

![[Pasted image 20210819023519.png]]

---
# FLAG.txt
![[Pasted image 20210819023601.png]]