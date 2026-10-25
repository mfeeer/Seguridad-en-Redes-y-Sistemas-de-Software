## Descripción
Can you decrypt this message? Decrypt this [message](https://challenge-files.cylabacademy.net/library/1415ede8e9f58b36fddf7b520d73c151a53ac100c476ca97c7a19f9b901100d3/cipher.txt) using this key "CYLAB".

pistas:
[https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher](https://en.wikipedia.org/wiki/Vigen%C3%A8re_cipher)
## Solución
```
Fer@Fersita:~$ wget https://challenge-files.cylabacademy.net/library/1415ede8e9f58b36fddf7b520d73c151a53ac100c476ca97c7a19f9b901100d3/cipher.txt
--2026-10-24 20:12:10--  https://challenge-files.cylabacademy.net/library/1415ede8e9f58b36fddf7b520d73c151a53ac100c476ca97c7a19f9b901100d3/cipher.txt
Resolving challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)... 13.226.187.40, 13.226.187.66, 13.226.187.37, ...
Connecting to challenge-files.cylabacademy.net (challenge-files.cylabacademy.net)|13.226.187.40|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 43 [application/octet-stream]
Saving to: ‘cipher.txt’

cipher.txt                    100%[=================================================>]      43  --.-KB/s    in 0s

2026-10-24 20:12:10 (25.7 MB/s) - ‘cipher.txt’ saved [43/43]


[0.381s] --> [0]
Fer@Fersita:~$ cat cipher.txt
caldfow{O0NU_WQ3_G1G3O3T3_A1AH3S_a0393cd7}

- una vez visto la flag, la decodificamos con vigenere decode en cyberchef, lo que nos da la flag:
  academy{D0NT_US3_V1G3N3R3_C1PH3R_y0393es7}
  
```
## Notas adicionales
- el nombre del reto nos dio la pista que el mensaje codificado era con vigenere, asismismo el reto nos daba la key clave para pode obtener la flag correspondiente
## Referencias
https://gchq.github.io/CyberChef/#recipe=Vigen%C3%A8re_Decode('CYLAB')&input=Y2FsZGZvd3tPME5VX1dRM19HMUczTzNUM19BMUFIM1NfYTAzOTNjZDd9