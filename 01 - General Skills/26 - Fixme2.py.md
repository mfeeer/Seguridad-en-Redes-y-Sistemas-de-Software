## Descripción
Fix the syntax error in the Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)

pistas:

1. Are equality and assignment the same symbol?

2. To view the file in the webshell, do: `$ nano fixme2.py`

3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.

4. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
Fers-academy@webshell:~$ nano fixme2.py
Fers-academy@webshell:~$ python3 fixme2.py
  File "/home/Fers-academy/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
ers-academy@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
```

## Notas adicionales
aquí descargamos el archivo y corregimos la línea 22 con la comparación if =, para que sea válida con un if ==
## Referencias