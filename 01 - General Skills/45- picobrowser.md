## Descripción
This website can be rendered only by picobrowser, go and catch the flag!

[http://fickle-tempest.picoctf.net:65006](http://fickle-tempest.picoctf.net:65006/)

Pistas:

1. You don't need to download a new web browser
## Solución
- En la pestaña network de la parte de herramientas para desarrollador podemos encontrar que la página identifica nuestro User-Agent para hacer la validación. Buscamos las network conditions y aquí buscamos custom user-agent, escribimos picobrowser y obtenemos la flag
picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}
## Notas adicionales
## Referencias
