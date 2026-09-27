
## Descripción
Can you get the flag? Go to this [website](http://xebec.cylabacademy.net:22665/) and see what you can discover.

pistas:
1. How is the password checked on this website?
## Solución

- Al entrar al link de este reto nos muestra un login
- al entrar nos dirá que el login fue fallido, la pista nos pregunta el como verificará la contraseña el sitio, podemos inspeccionar el sitio con el fin de buscar una vulnerabilidad (sources)
- Cuando nos regresa la contraseña encontraremos un archivo secure.js con el siguiente código:

```js
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

- con este codigo podemos obtener el username y la contraseña con las cuales debemos entrar al sitio y eso nos arroja la flag correspondiente:
 academy{j5_15_7r4n5p4r3n7_df9583b6} 
## Notas adicionales
## Referencias
