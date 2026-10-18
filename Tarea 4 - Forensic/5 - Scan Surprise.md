## Descripción
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?

You can download the challenge files here:

- [challenge.zip](https://challenge-files.cylabacademy.net/library/55c0e897129786cdc2c3f7c8f08e346866d9c187f20adf8b2f22a0ed2fe76e37/challenge.zip) The same files are accessible via SSH here:

`ssh -p 36126 ctf-player@xebec.cylabacademy.net`

Using the password `fd7746b4`. Accept the fingerprint with `yes`; the QR code prints as soon as you connect, and `ls` will show the same image as `flag.png`. Remember, in a shell, passwords are hidden!


1. QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.

2. Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11

3. If you don't have access to a phone, you can also use zbar-tools to convert an image to text
## Solución
Primero descargamos el .zip que se nos da y lo descomprimimos, después accedemos hasta el código qr y lo escaneamos con un celular y el gmail que nos da, es la flag
```
academy{p33k_@_b00_5f0d36e7}
```
## Notas adicionales
## Referencias