## Descripción
How to automate tasks to run at intervals on linux servers?

Use ssh to connect to this server:

`Server: saturn.picoctf.net Port: 57527 Username: picoplayer Password: kZx-HVJKu8`
## Solución
```
Fers-academy@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 57527 
picoplayer@challenge:~$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```
## Notas adicionales
- para este reto ocupamos activar la conexión con el puerto y contraseña dados
- despues accedemos a la carpeta de configuraciones de tiempo del usuario picoplayer
- el cat nos permite ver nuestra flag.
## Referencias