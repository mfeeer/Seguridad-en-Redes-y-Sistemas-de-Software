## Descripción

Decode this [message](https://challenge-files.cylabacademy.net/library/d825fde6581b1311eafdd403da1cc96f1f98fe3fe84cd71d850310ebb3908088/message.wav) from the moon.

pistas:

1. How did pictures from the moon landing get sent back to Earth?

2. What is the CMU mascot?, that might help select a RX option
## Solución
Descargaremos la herramienta para hacer uso del sstv, tras descargarla haremos lo siguiente:

```
wget https://challenge-files.picoctf.net/c_fickle_tempest/678ff56c639c7645276578f3a9767ec2feaed1450045dd982c525b5795f7f589/message.wav
sstv -d message.wav -o result.png

picoCTF{beep_boop_im_in_space}
```

Nuestra imagen estará volteada, por lo que solo hay que girarla con el editor de imágenes de kali y con eso se nos mostrará la imagen.

## Notas adicionales
## Referencias
