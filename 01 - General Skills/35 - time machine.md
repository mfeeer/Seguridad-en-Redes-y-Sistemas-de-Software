## Descripción
What was I last working on? I remember writing a note to help me remember...

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/66/challenge.zip)

Pistas:

1. The `cat` command will let you read a file, but that won't help you here!

2. Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).

3. When committing a file with git, a message can (and should) be included.

## Solución
```
Fers-academy@webshell:~/drop-in$ wget https://artifacts.picoctf.net/c_titan/66/challenge.zip
Fers-academy@webshell:~/drop-in$ unzip challenge.zip
Fers-academy@webshell:~/drop-in$ cd drop-in
Fers-academy@webshell:~/drop-in/drop-in$ git log
```
## Notas adicionales
- este reto fue igual que el pasado
- aqui nos ahorramos el git checkout ya que al hacer git log ya se veía la flag
## Referencias