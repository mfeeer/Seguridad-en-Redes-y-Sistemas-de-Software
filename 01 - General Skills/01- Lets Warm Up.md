## Descripción
if I told you Word started with 0x70 in hexadecimal, what would it start with in ASCII?


## Solución:
Ir al sitio web rapidtables

picoCTF{p}

C:\Users\usuario>py
Python 3.14.2 (tags/v3.14.2:df79316, Dec  5 2025, 17:18:21) [MSC v.1944 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> int (0x70)
112
>>> chr(112)
'p'
>>> ord('p')
112

picoCTF{p}
## Notas adicionales:
Siempre hay que tener en cuenta el formato de la bandera para que sea aceptada

## Referencias:
https://www.rapidtables.com/convert/number/hex-to-ascii.html