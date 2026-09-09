## Descripción
There is some interesting information hidden around this site. Can you find it?

http://wily-courier.picoctf.net:50411/

Pistas:
1. You should have enough hints to find the files, don't run a brute forcer.
## Solución

```
1. el primer paso fue entrar al link que se proporciona en el reto
2. al entrar inspeccionamos el codigo y se encontraba la primera parte de la flag
3. despues entramos al .cs en donde encontramos la segunda parte
4. vimos que en el archivo .js no estaba ninguna flag, asi que a nuestra url le agregamos robots.txt para obtener la tercera parte
5. agregamos este comando en la terminal  curl -s http://wily-courier.picoctf.net:50411/.htaccess
# Part 4: 3s_2_lO0k
y obtenemos la parte 4
6. por ultimo este comando curl -s http://wily-courier.picoctf.net:50411/.DS_Store
Congrats! You've completed the scavenger hunt! Part 5: _9588550}
que nos da la 5ta y ultima parte
y unimos:
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}
```

## Notas adicionales

## Referencias
