## Descripción

Can you look at the data in this binary? The bash script might help!
## Solución
```
wget https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/static

wget https://challenge-files.picoctf.net/c_wily_courier/418e2775a501eaabeb99a96c5c467a83539369fe9649e8234644250cfb72d717/ltdis.sh

 echo $0
-bash
Fers-academy@webshell:~$ chmod +x ltdis.sh
Fers-academy@webshell:~$ ./ltdis.sh
Attempting disassembly of  ...
Fers-academy@webshell:~$ ./ltdis.sh static
Attempting disassembly of static ...
Disassembly successful! Available at: static.ltdis.x86_64.txt
Ripping strings from binary with file offsets...
Any strings found in static have been written to static.ltdis.strings.txt with file offset
Fers-academy@webshell:~$ cat static.ltdis.x86_64.txt | grep pico
Fers-academy@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_20335e41}

```


## Notas adicionales

- .sh son archivos que contienen comandos de linux agrupados, se les llama, scripts de bash
- rm * borra todos los archivos en la carpeta actual 
- rm -rf * - borra todos los archivos y carpetas dentro de la carpeta actual, sin preguntar

## Referencias
