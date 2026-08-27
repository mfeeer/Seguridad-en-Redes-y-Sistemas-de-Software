## Descripción
Fix the syntax error in this Python script to print the flag.

[Download Python script](https://artifacts.picoctf.net/c/26/fixme1.py)

pistas:

1. Indentation is very meaningful in Python

2. To view the file in the webshell, do: `$ nano fixme1.py`

3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.

4. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/26/fixme1.py
python3 fixme1.py
  File "/home/Fers-academy/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
Fers-academy@webshell:~$ nano fixme1.py                              
Fers-academy@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
```


## Notas adicionales
lo que se hizo en este ejercicio fue descargar el archivo.
- al ejecutarlo en la terminal nos muestra el tipo de error
- se corrigió la indentación de la línea 20 y con eso nos dio la flag correspodiente
## Referencias