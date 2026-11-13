## Descripción
The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://challenge-files.cylabacademy.net/library/6dfc63d7e4ee66dec270d4f50ae9e6c2b1ed3c6364b723c94f23210d2ab91740/need-for-speed)


1. What is the final key?
## Solución

```
descargamos el archivo
una vez descargado ejecutamos los siguiente comandos:
chmod +x need-for-speed
gdb ./need-for-speed
Dentro de gdb:

(gdb) handle SIGALRM ignore
(gdb) run
y nos arroja la flag correspondiente:
academy{Good job keeping bus #31b86b76 speeding along!}
```
## Notas adicionales
## Referencias
