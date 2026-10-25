## Descripción

This service provides you an encrypted flag. Can you decrypt it with just N & e? Connect to the program with netcat:

`$ nc chatelaine.cylabacademy.net 47544`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/742b4d10be646510247831837d9876dafee7f7eb0eea7ee82eaf8f04981ef2d3/encrypt.py).
 pistas:

1. How much do we trust randomness?

2. Notice anything interesting about N?

3. Try comparing N across multiple requests
## Solución

```
- Me conecté al servicio con `nc chatelaine.cylabacademy.net 47544` y obtuve n y e y el texto cifrado.
    
- Observé que n era par, por lo que uno de sus factores era p=2.
    
- Calculé q=n/2 y comprobé que era primo.
    
- Calculé \(\varphi(N)=q-1\) y obtuve la clave privada mediante \(d=e^{-1}\bmod\varphi(N)\).
    
- Descifré el texto con \(m=c^d\bmod N\) y convertí el resultado a bytes.

- Obtuve la flag:
  academy{tw0_1$_pr!m39cf1fb4f}
```
## Notas adicionales
## Referencias
