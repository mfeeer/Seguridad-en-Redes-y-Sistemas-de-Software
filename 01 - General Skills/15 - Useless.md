## Descripción
There's an interesting script in the user's home directory
The work computer is running SSH. We've been given a script which performs some basic calculations, explore the script and find a flag.
saturn.picoctf.net Port: 49618 Username: picoplayer Password: password
## Solución
```
ssh picoplayer@saturn.picoctf.net -p 49979
The authenticity of host '[saturn.picoctf.net]:49979 ([13.59.203.175]:49979)' can't be established.
ED25519 key fingerprint is SHA256:DiJcS90U9QussLS8HLR6l6BGJb5eCA0vRmA18IvDvw8.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:2: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:49979' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 

picoplayer@challenge:~$ ls
useless
picoplayer@challenge:~$ cat useless
#!/bin/bash
# Basic mathematical operations via command-line arguments
    This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6140}
man useless

```

## Notas adicionales


## Referencias
