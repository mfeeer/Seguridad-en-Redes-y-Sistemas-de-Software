## Descripción
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://challenge-files.cylabacademy.net/library/7f760cee144ac7237469fd6bfab7c748d6f1d101ca47c101187ca7d8f5c721f0/leak.tar).

The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

pistas:
1. Maybe other passwords will have hints about the leak?

## Solución
```
- Descomprimí `leak.tar` para obtener los archivos de usuarios y contraseñas.
    
- Busqué `cultiris` en `usernames.txt` con `grep -n` y encontré que estaba en la línea 378.
    
- Consulté la línea 378 de `passwords.txt` con `sed` y obtuve la contraseña cifrada.
    
- Identifiqué que estaba usando ROT13 y utilicé cyberchef para decodificar la flag
    
- Recuperé la flag:

`academy{C7r1F_54V35_71M3}`
```

## Notas adicionales

## Referencias
