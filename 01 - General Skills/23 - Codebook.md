## Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)
pistas:
1. On the webshell, use `ls` to see if both files are in the directory you are in

2. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py

Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt

Fers-academy@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}

## Notas adicionales

- se descargaron los dos archivos proporcionados, para después ejecutar code.py y que nos arroja la flag correspondiente.
## Referencias