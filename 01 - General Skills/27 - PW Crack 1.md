## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

pistas:

1. To view the file in the webshell, do: `$ nano level1.py`

2. To exit `nano`, press Ctrl and x and follow the on-screen prompts.

3. The `str_xor` function does not need to be reverse engineered for this challenge.

## Solución
```
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.py

Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/11/level1.flag.txt.enc
 nano level1.py
Fers-academy@webshell:~$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```
## Notas adicionales
- descargamos ambos archivos
- buscamos la contraseña que nos pide el archivo, al entrar al documento se puede ser cual es, se pone en donde corresponde y obtenemos la flag.
## Referencias