## Descripción
We have recovered a [binary](https://challenge-files.cylabacademy.net/library/5c6cabcc52da3ddc1032e6ff4b73c25c2115f1a3f462d63c112c36e1fefcc892/rev) and a [text file](https://challenge-files.cylabacademy.net/library/5c6cabcc52da3ddc1032e6ff4b73c25c2115f1a3f462d63c112c36e1fefcc892/rev_this). Can you reverse the flag.

pistas:

1. objdump and Gihdra are some tools that could assist with this
## Solución
```
1. Descargar ambos archivos: `rev` y `rev_this`.
2. Ver el contenido de `rev_this` con `cat rev_this`. Sale la flag cifrada: `academy{w1{1wq83;4<1h_6}`.
3. Abrir el binario `rev` en Ghidra (o desensamblarlo con `objdump -d rev`) y analizar la función `main`.
4. En el código se ve que el programa:
   - Copia sin cambios los primeros 8 caracteres (`academy{`).
   - Del carácter 8 al 22: si la posición es **par**, le **suma 5**; si es **impar**, le **resta 2**.
   - Copia sin cambios el último carácter (`}`).
5. Para revertirlo se aplica la operación contraria: posición par **−5**, posición impar **+2**.
6. Script en Python para descifrar:
   ```python
   s = "academy{w1{1wq83;4<1h_6}"
   flag = s[:8]
   for i in range(8, 23):
       flag += chr(ord(s[i]) - 5) if i % 2 == 0 else chr(ord(s[i]) + 2)
   flag += s[23]
   print(flag)

academy{r3v3rs356673ca1}
```
## Notas adicionales
## Referencias
https://ghidra-sre.org/

https://www.asciitable.com/