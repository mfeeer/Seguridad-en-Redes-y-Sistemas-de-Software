## Descripción
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://challenge-files.cylabacademy.net/library/7459f4a2a283307f76c6bf1b035e6f99a63123c791891ddaeb97ade552711f22/VaultDoor1.java)

pistas:
1. Look up the charAt() method online.
## Solución
```
descargamos el archivo, una vez descargado, ejecutamos el siguiente comando:
 cat VaultDoor1.java | grep "charAt" | sed "s/.*charAt(\([0-9]*\)).*'\([^']*\)'.*/\1 \2/" | sort -n | awk
'{print $2}' | tr -d '\n'
lo que nos da la flag:
academy{d35cr4mbl3_tH3_cH4r4cT3r5_724ca5}



```
## Notas adicionales
## Referencias
