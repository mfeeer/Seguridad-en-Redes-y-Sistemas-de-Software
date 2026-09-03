## Descripción
Can you break into this super secure portal?

[http://fickle-tempest.picoctf.net:56391](http://fickle-tempest.picoctf.net:56391/)

Pistas:

1. Never trust the client

## Solución
- Al entrar al link, encontramos solamente un fondo azul con una caja donde podemos introducir una contraseña, al ingresar cualquier palabra (menos la bandera) nos dará un error donde nos dice que la contraseña está incorrecta, al abrir el código fuente de la página la función verify(), tiene una estructura que no está en orden, para eso tenemos que ordenar la secuencia de los splits y asi encontramos la flag.

## Notas adicionales
## Referencias
