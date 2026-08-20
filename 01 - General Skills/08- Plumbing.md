## Descripción

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?
Connect to fickle-tempest.picoctf.net 54947.
pista:
1

Remember the flag format is picoCTF{XXXX}

2

What's a pipe? No not that kind of pipe... This kind
## Solución
´´´
Fers-academy@webshell:~$ nc fickle-tempest.picoctf.net 54947 | grep pico
picoCTF{digital_plumb3r_0BAc587E}
´´´
## Notas adicionales
- python utiliza el + para concatenar cadenas
- chr() es una función de python que convierte un numero a su correspondiente caracter ASCII
- esto fue simplemente una suma de cadenas y caracteres
## Referencias