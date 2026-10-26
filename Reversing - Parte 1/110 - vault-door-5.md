## Descripción

In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://challenge-files.cylabacademy.net/library/d085790fcd0c6bfae8d8e539ae372300b7da193466d0d499d4653621fc485a7c/VaultDoor5.java)

pistas:

1. You may find an encoder/decoder tool helpful, such as [https://encoding.tools/](https://encoding.tools/)

2. Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.

## Solución

```

El código le hace al password dos vueltas: primero lo convierte a URL-encoding (`%XX` por cada byte) y luego eso lo pasa a Base64, y compara contra un string fijo. Entonces lo hice al revés: decodifiqué el Base64 del `expected` y me quedó puro texto tipo `%63%30%6e...`; cada `%XX` es un carácter en hex, así que fui convirtiendo cada uno a su letra (ej. `%63` = `c`). Uniendo todo me dio `c0nv3rt1ng_fr0m_ba5e_64_75865cc3` (“converting_from_base_64_” + el sufijo random), y ese es el password.
fuimos a cyberchef para ayudatnos a decodificar y nos da la flag:
academy{c0nv3rt1ng_fr0m_ba5e_64_75865cc3}
```
## Notas adicionales
## Referencias
