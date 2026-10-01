## Descripción

I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.cylabacademy.net/library/4a463561643f2cc25e74665dadd7ca654a9b828dc7a5b9239a8000ab4179c57e/whitepages.txt) is all blank!

Pistas:

1. There is data encoded somewhere... there might be an online decoder.
## Solución
Para esta solución se debió de instalar pwntools para python se puede usar este comando:

```
 sudo apt install python3-pwntools
```

Ahora, podemos crear un script de python que nos resuelva el reto

```
from pwn import *

file = open('whitepages.txt', 'rb')
data = bytearray(file.read())
data = data.replace(b'\xe2\x80\x83', b'0')
data = data.replace(b'\x20', b'1')
data = data.decode('ascii')
data = unbits(data)

print(data)
```
## Notas adicionales
## Referencias
