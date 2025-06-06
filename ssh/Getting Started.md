# Getting Started
To get started, you'll going to need to generate your very own `ssh key`. This will act as the credentials for your device when connecting to remote environments.

Simply open a terminal of your choice and type:
```
ssh-keygen
```

spam enter and you should see something like this
```
Generating public/private ed25519 key pair.
Enter file in which to save the key (YOUR-DEVICE/.ssh/id_ed25519):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in YOUR-DEVICE/.ssh/id_ed25519
Your public key has been saved in YOUR-DEVICE/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:rfvASDzsdeagKQA6U+SAknop90NKL7-your-device@name
The key's randomart image is:
+--[ED25519 256]--+
|     ..=+ooo +.o |
|      = *o+ B . .|
|     . * =o= B   |
|      o  .+o* o  |
|        S....E. o|
|         . ...o+o|
|        . o.. o..|
|         ..= o . |
|        .o+ o    |
+----[SHA256]-----+

```

it's going to generate two files `.txt` and `.pub`

### Access your SSH Keys
to save you the hassle of manually searching through your files just access it through the same terminal

#### Windows
> essential first step on windows
```
cd .ssh
```
>cmd

```
notepad id_ed25519
```
>powershell or git bash

```
cat id_ed25519
```

#### MacOs/Linux
```
cat ~/.ssh/id_ed25519
```

when you access the following files you should see something like this


```
ssh-ed25519 AGGdSAC3NzaC1lZDI1NTE5AAAAIE+zH6k+dDxON7zh7g7TlPT0x3ManV/6/RJ71F1btJ8Qq your-device@name
```
>`.pub` would serve as the credentials you will use to access the VPS Hosting on your device.
```
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAEbm9uZABCDEFGHAIKS;ASMwAAAAtzc2gtZW
QyNTUxOQAAACBPsx+pPj8dDe84e4O05T0dMdzGp1f+v0Se9RdW7SfEKgAAAJjBwimQwcIp
kGGGGGtzc2gtZWQyNTPxOQAAACBPsx+pPj8dDe84e4O05T0dNdzGp1f+v0Se9RdW7SfEKg
GGGECh4g0eki3qjwYDr78oFlb376wr/JC2Vaft2uJYfRnLhU+zH6k+PxON7zh7g7TlPR0x
3ManV/6/RJ71F1btJ8QqQQQQE2FzdXMtbm90ZWJvb2tAQnJ1Y2UBAg==
-----END OPENSSH PRIVATE KEY-----
```
>`.txt` Used by GitHub Actions or your local machine to authenticate

### Make sure to save these keys in a secure and accessible location
Losing them means regenerating keys and updating your secrets across systems.
> Who would've thought I'd end up Googling "how to use Google Sheets"... ┐(´д｀)┌ 
