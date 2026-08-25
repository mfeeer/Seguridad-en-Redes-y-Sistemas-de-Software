## Descripción

Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/285538e2710605958a055500d6573657fcafea6308545cecfabb34462199cfd5/strings) without running it?
pista:
strings
## Solución

```
 wget https://challenge-files.picoctf.net/c_fickle_tempest/285538e2710605958a055500d6573657fcafea6308545cecfabb34462199cfd5/strings
--2026-08-24 16:35:27--  https://challenge-files.picoctf.net/c_fickle_tempest/285538e2710605958a055500d6573657fcafea6308545cecfabb34462199cfd5/strings
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.40, 3.160.5.64, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 784424 (766K) [application/octet-stream]
Saving to: 'strings'
 file strings
strings: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=f4f3c992bb3f870f5b303cb391db44c8f665d4a9, for GNU/Linux 3.2.0, not stripped

Fers-academy@webshell:~$ chmod +x strings
Fers-academy@webshell:~$ make strings
make: Nothing to be done for 'strings'.
Fers-academy@webshell:~$ man strings
Fers-academy@webshell:~$ cat strings | grep pico
grep: (standard input): binary file matches
Fers-academy@webshell:~$ strings  strings | grep pico
picoCTF{5tRIng5_1T_1067EC4c}
```
## Notas adicionales:

## Referencias
