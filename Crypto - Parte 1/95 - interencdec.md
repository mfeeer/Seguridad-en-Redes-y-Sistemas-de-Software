## Descripción

Can you get the real meaning from this file.

Download the file [here](https://challenge-files.cylabacademy.net/library/0d5754d51dc425dbb46c76eef33bb2b596a1a3bc6f4163ddd2a215f7e0d45198/enc_flag).

1. Engaging in various decoding processes is of utmost importance
## Solución
Al abrir el archivo encontraremos una cadena en base 64 (por los 2 = que están al final), al [decodificarla](https://toolbox.itsec.tamu.edu/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=WWlka00wSnhaR3R3UWxSWWRIRmhSM2cyWVVoc1ptRjZUbkZsVkd3eldWUk9jbGd5TUhkTmFrVjVUbnBWTkdaUlBUMG5DZz09) encontraremos otra cadena en base 64, la [decodificamos](https://toolbox.itsec.tamu.edu/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true,false\)&input=ZDNCcWRrcEJUWHRxYUd4NmFIbGZhek5xZVRsM1lUTnJYMjB3TWpFeU56VTRmUT09) y encontramos el formato de la flag. Aquí podemos intentar algunos métodos de desencriptación, pero lo más inteligente es meterlo a un identificador, nos dió caesar, por lo que encontramos nuestra flag.
academy{caesar_d3cr9pt3d_81ed9f02}
## Notas adicionales
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=aGpoa2x0ZntqaGx6aHlfazNqeTl3YTNrXzgxbGs5bTAyfQ0K&ieol=CRLF&oeol=CRLF

## Referencias
