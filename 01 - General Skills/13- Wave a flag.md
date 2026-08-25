## Descripción
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...
1. This program will only work in the webshell or another Linux computer.

2. To get the file accessible in your shell, enter the following in the Terminal prompt: $ wget, where the url can be found in the details section.

3. Run this program by entering the following in the Terminal prompt: $ ./warm, but you'll first have to make it executable with $ chmod +x warm

4. -h and --help are the most common arguments to give to programs to get more information from them!

5. Not every program implements help features like -h and --help.
## Solución
```
Fers-academy@webshell:~$ chmod +x warm   
Fers-academy@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```
## Notas adicionales
- El comando chmod +x warm otorga permisos de ejecución al archivo llamado warm
## Referencias
