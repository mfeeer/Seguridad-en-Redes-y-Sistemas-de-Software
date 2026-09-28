## Descripción
This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.cylabacademy.net/library/e78198c6a7dc5e471e8429d4953e7595feafe17764258eec169b8dab8bb3c925/garden.jpg).

1. What is a hex editor?
## Solución
```
descargamos la imagen con:
wget https://challenge-files.cylabacademy.net/library/e78198c6a7dc5e471e8429d4953e7595feafe17764258eec169b8dab8bb3c925/garden.jpg

mostramos la cadena de la imagen:
strings -n 10 garden.jpg 

encontramos la flag:
academy{more_than_m33ts_the_3y3e23d7ba9}
```

## Notas adicionales
- al ejecutar el comando  strings -n 10 garden.jpg me marcó error por no tener instalado sudo apt install binutils, solo ejecuté eso y ya se logró ver la flag correspondiente.
- el comando strings  --saca las cadenas de una imagen
- si queremos encontrar solo la flag sin toda la cadena ejecutamos este comando strings garden.jpg -n 15 | grep academy

## Referencias
