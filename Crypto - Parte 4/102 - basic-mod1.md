## Descripción
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://challenge-files.cylabacademy.net/library/23b095a85da350dcda44aefdf5a62785a023f5d4570374d08eef71aefd096f7f/message.txt).

Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.

Wrap your decrypted message in the academy flag format (i.e. `academy{decrypted_message}`)

pistas:
1. Do you know what `mod 37` means?

2. `mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.
## Solución

Usamos este script:

```python
message= "91 396 316 198 225 369 50 369 350 63 205 346 299 406 330 397 335>
message = message.split(" ")
alfabeto = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789_"
resultado = "academy{"
for char in message:
    resultado += alfabeto[int(char) % 37]
resultado += "}"
print(resultado)

```

encontramos la flag:
academy{R0UND_N_R0UND_81CE8A51}
## Notas adicionales
## Referencias
