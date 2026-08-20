## Descripción
Can you find the flag in the file? This would be really tedious to look through manually, something tells me there is a better way.

pista:
grep tutorial
## Solución
´´´
Fers-academy@webshell:~$ wget https://challenge-files.picoctf.net/c_fickle_tempest/b8915fc817a2cd58e83d7e779515ed3f898738d12cf1974086f8ba3f515ae3cf/file
--2026-08-19 16:49:08--  https://challenge-files.picoctf.net/c_fickle_tempest/b8915fc817a2cd58e83d7e779515ed3f898738d12cf1974086f8ba3f515ae3cf/file
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.64, 3.160.5.95, 3.160.5.40, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.64|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14546 (14K) [application/octet-stream]
Saving to: 'file'

Fers-academy@webshell:~$ cat file | grep picoCTF
´´´
picoCTF{grep_is_good_to_find_things_beD770f5}


## Notas adicionales

## Referencias
