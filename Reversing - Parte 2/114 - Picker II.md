## Descripción

Can you figure out how this program works to get the flag? Connect to the program with netcat:

`$ nc xebec.cylabacademy.net 13896`

The program's source code can be downloaded [here](https://challenge-files.cylabacademy.net/library/4210d9f2819181aa8a3214d0155e8eb7d0eaa900859eca24816e0f96e7548ae0/picker-II.py).
## Solución
```
Al conectarnos introduciremos `print(open('flag.txt','r').read())` lo cual nos mostrará la flag.

academy{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_e9683452}
```
## Notas adicionales
## Referencias
