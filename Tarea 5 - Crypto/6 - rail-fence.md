## Descripción
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message [here](https://challenge-files.cylabacademy.net/library/d6cea3d41550d2d3e365dd3a7ea99fe9b44fe5fa437d1c921b5134a2070894a5/message.txt).

The decoded message names a phrase. Put that phrase, and nothing else, in the academy flag format: `academy{phrase}`.

pistas:
1. Once you've understood how the cipher works, it's best to draw it out yourself on paper

## Solución
```
-Descargamos el archivo y una vez descargado ejecutamos:
cat message.txt
nos da el mensaje descifrado y una vez descifrado obtenemos la flag:

academy {WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_43BBCEC4}

```

o podemos usar este script: 
```python
cat > message.py <<'PY'
texto = open("message.txt").read().strip()
patron = list(range(4)) + list(range(2, 0, -1))
orden = [patron[i % len(patron)] for i in range(len(texto))]

cantidades = [orden.count(r) for r in range(4)]
rieles = []
inicio = 0

for cantidad in cantidades:
    rieles.append(list(texto[inicio:inicio + cantidad]))
    inicio += cantidad

posiciones = [0, 0, 0, 0]
resultado = ""

for r in orden:
    resultado += rieles[r][posiciones[r]]
    posiciones[r] += 1

print("Mensaje descifrado:", resultado)
PY
python3 message.py
```
## Notas adicionales
## Referencias
