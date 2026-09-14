## Descripción
Check the admin scratchpad!

[http://fickle-tempest.picoctf.net:54167](http://fickle-tempest.picoctf.net:54167/)


Pistas:
1. What is that cookie?

2. Have you heard of JWT?
## Solución

```
La pista del reto nos sugiere el uso de las cookies, por lo que se volverá a usar la extensión que se usó en el reto 8 - Cookies, entonces, si buscamos en las cookies tras habernos "registrado" en la página, encontramos una cookie llamada jwt, la cual si la buscamos en un [decodificador o codificador JWT](https://www.jwt.io/) nos mostrará una cadena con bastantes digítos. Para esto, usaremos la biblioteca john, enfocada en crackear contraseñas. Se usa el archivo rockyou.txt (alojado en `/usr/share/wordlists`, cabe avisar que se debe de descomprimir con `gzip -d /usr/share/wordlists/rockyou.txt.gz`), ahora, se aplica el siguiente comando:
john -w=/usr/share/wordlists/rockyou.txt
Esto nos da una contraseña: ilovepico 
lo que nos permite que podamos ingresar como admin y nos muestre la flag que es:
picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
```
## Notas adicionales
- se recomienda utilizar kali linux para evitar problemas con los comandos correspondientes
## Referencias
