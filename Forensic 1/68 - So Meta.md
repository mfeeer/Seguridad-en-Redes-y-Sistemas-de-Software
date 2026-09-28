## Descripción
Find the flag in this [picture](https://challenge-files.cylabacademy.net/library/8179732d3bcbaaf9dadfc7fe08aa5b7fbf1d3189b0a2dc90eca34dca38a85b4a/pico_img.png).

1. What does meta mean in the context of files?

2. Ever heard of metadata?
## Solución

```
wget https://challenge-files.cylabacademy.net/library/8179732d3bcbaaf9dadfc7fe08aa5b7fbf1d3189b0a2dc90eca34dca38a85b4a/pico_img.png

open pico_img.png

exiftool -Artist pico_img.png
Artist                          : academy{s0_m3ta_45015e26}

(Fer㉿Fersita)-[~]
└─$ strings -n 20 pico_img.png | grep academy
academy{s0_m3ta_45015e26}

```
## Notas adicionales
- exiftool sirve para ver los metadatos dentro del archivo
- -Artist es un filtro, en lugar de arrojar toda la list de los metadatos, le indica al programa que solo le interesa ver lo que está escrito en el campo "Artista"
## Referencias