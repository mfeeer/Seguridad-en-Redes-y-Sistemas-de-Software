## Descripción
Can you crack the password to get the flag?

Download the password checker [here](https://artifacts.picoctf.net/c/17/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/17/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/17/level3.hash.bin) in the same directory too.

There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

pistas:

1. To view the level3.hash.bin file in the webshell, do: `$ bvi level3.hash.bin`

2. To exit `bvi` type `:q` and press enter.

3. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.py

Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.flag.txt.enc

Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/17/level3.hash.bin
Fers-academy@webshell:~$ nano level3.py
Fers-academy@webshell:~$ python3 level3.py
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```
## Notas adicionales
- se modificó la función donde checaba la contraseña para que en vez de tener que probar las 7 posibles contraseñas una por una, con un bucle for haga las combinaciones posibles para obtener la correcta
## Referencias