## Descripción
I accidentally wrote the flag down. Good thing I deleted it!

You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/76/challenge.zip)

pistas:
1. Version control can help you recover files if you change or lose them!

2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)

3. You can 'checkout' commits to see the files inside them
## Solución
```
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c_titan/76/challenge.zip
Fers-academy@webshell:~$ unzip challenge.zip
Fers-academy@webshell:~$ cd drop-in
Fers-academy@webshell:~/drop-in$ git log
Fers-academy@webshell:~/drop-in$ git checkout e720dc26a1a55405fbdf4d338d465335c439fb3e
Fers-academy@webshell:~/drop-in$ nano message.txt
```
## Notas adicionales
- al hacer git log abrí los commits en el log del git, en donde apareció mi commit especifico
- al hacer el nano en ese commit salió la flag correspondiente
## Referencias