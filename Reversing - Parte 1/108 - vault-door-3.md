## Descripción

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://challenge-files.cylabacademy.net/library/64ed47ea66574a28e2f23bbe36be348987a9ff131641bf451b1c04bb7b3e2d9f/VaultDoor3.java)

pistas:

1. Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.
## Solución
usamos el siguiente script:

```python
target = "jU5t_a_sna_3lpm11g54e_u_4_m4r042"
flag = [''] * 32

# Replicamos la lógica del código Java para reconstruir el original
for i in range(0, 8):
    flag[i] = target[i]

for i in range(8, 16):
    flag[23-i] = target[i]

for i in range(16, 32, 2):
    flag[46-i] = target[i]

for i in range(31, 16, -2):
    flag[i] = target[i]

print("picoCTF{" + "".join(flag) + "}")


```
## Notas adicionales
## Referencias
