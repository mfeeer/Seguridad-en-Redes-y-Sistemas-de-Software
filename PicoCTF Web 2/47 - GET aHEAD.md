## Descripción
Find the flag being held on this server to get ahead of the competition

http://wily-courier.picoctf.net:59101/

Pistas:
1. Maybe you have more than 2 choices

2. Check out tools like Burpsuite to modify your requests and look at the responses
## Solución

```
Fers-academy@webshell:~$ curl -s GET  http://wily-courier.picoctf.net:59101/index.php
Fers-academy@webshell:~$ curl -s -X POST  http://wily-courier.picoctf.net:59101/index.php
Fers-academy@webshell:~$ curl -s -I  http://wily-courier.picoctf.net:59101/index.php
HTTP/1.1 200 OK
Date: Mon, 07 Sep 2026 16:23:14 GMT
Server: Apache/2.4.38 (Debian)
X-Powered-By: PHP/7.2.34
flag: picoCTF{r3j3ct_th3_du4l1ty_8b13f07}
Content-Type: text/html; charset=UTF-8
```

## Notas adicionales
- se le puede pedir a la IA que nos de un código que implemente eso para poder obtener la flag correspondiente
## Referencias
