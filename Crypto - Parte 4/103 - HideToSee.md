## Descripción
How about some hide and seek heh? Look at this image [here](https://challenge-files.cylabacademy.net/library/771a76c980170940b6bce49ef90b4fbcbaafc74b555625fec08aca0dd2ecae2c/atbash.jpg).

pistas:

1. Download the image and try to extract it.
## Solución

```
Descargamos el archivo y una vez descargado y abierto, ajecutamos los siguientes comandos:

sudo apt install steghide
steghide --extract -sf atbash.jpg
cat encrypted.txt

nos da el mensaje codificado:
zxzwvnb{zgyzhs_xizxp_y1y5x980}

lo decodificamos con cyberchef y obtenemos la flag:

academy{atbash_crack_b1b5c980}
```

## Notas adicionales
## Referencias
https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=enh6d3ZuYnt6Z3l6aHNfeGl6eHBfeTF5NXg5ODB9