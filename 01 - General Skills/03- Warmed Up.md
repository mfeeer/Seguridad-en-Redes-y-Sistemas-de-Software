## Descripción
What is 0x3D (base 16) in decimal (base 10)?

pista:
Submit your answer in our flag format. For example, if your answer was '22', you would submit 'picoCTF{22}' as the flag.
## Solución
´´´
C:\Users\usuario>py
Python 3.14.2 (tags/v3.14.2:df79316, Dec  5 2025, 17:18:21) [MSC v.1944 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> int("0x3D", 16)
61
´´´

picoCTF{61}
## Notas adicionales
La función int, convierte cualuier numero a base 10, el segundo parámetro indica la base en la que está el número.

>>> int("052", 8)
42
>>> int("010101", 2)
21

## Referencias