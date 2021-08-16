# EXTERNAL

## FTP Anonymous Login
Getting and reading **note.txt**:

![[Pasted image 20210817023047.png]]

This could mean that we should focus on the user **pwnlab**

## FTP BRUTE FORCE (HYDRA)
![[Pasted image 20210817023843.png]]

## FTP (As pwnlab)
Loggin in as the user **pwnlab** will land you on his home directory

![[Pasted image 20210817024453.png]]


---

## HTTP

Visiting **/wordpress**, we are being redirected to another ip address:

![[Pasted image 20210817014947.png]]

We can fix this by using **BurpSuite**:

1) Open **BurpSuite**, go to **Options > Scroll down to "Match and Replace"**

![[Pasted image 20210817015114.png]]

Click **Add New** and select **Response Header**, add the IP where it redirects to **Match** and add the target IP to **Replace**

By re-visiting the page while the proxy is on, we should be able to fix **wordpress**:

![[Pasted image 20210817020754.png]]

---

## SSH (As pwnlab)

Trying the credentials of the user **pwnlab** that we found (refer to [[CREDENTIALS]]) against SSH, we should be able to get in

![[Pasted image 20210817024823.png]]

