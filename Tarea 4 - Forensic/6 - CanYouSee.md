## Descripción
How about some hide and seek?

Download this file [here](https://challenge-files.cylabacademy.net/library/9b029ae1f6eeb888f00d61f70ef1223afce75f409a25b0076838b9af310b66c3/unknown.zip).

pistas:
1. How can you view the information about the picture?

2. If something isn't in the expected form, maybe it deserves attention?
## Solución
Primero descargamos el archivo que se nos da y lo descomprimimos, después usamos exiftool en la imagen y con ello en "Attribution URL" esta la flag encriptada, la desencriptamos y obtenemos la flag
```
echo YWNhZGVteXtNRTc0RDQ3QV9ISUREM05fOTI3MTgzYjN9Cg== | base64 -d
academy{ME74D47A_HIDD3N_927183b3}

```
## Notas adicionales
## Referencias
