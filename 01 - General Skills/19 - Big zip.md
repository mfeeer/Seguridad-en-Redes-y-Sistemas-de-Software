## Descripción
Unzip this archive and find the flag.

## Solución
```
unzip big-zip-files.zip
find . -name "uber-secret.txt"
grep -r "picoCTF" big-zip-files/
picoCTF{gr3p_15_m4g1c_ef8790dc}
```
## Notas adicionales
- Descomprimir el archivo zip con unzip
- Después moverse a la carpeta con cd big-zip-files/
- hacer un grep -r para buscar el texto
## Referencias
https://shibushivansh.medium.com/picoctf-big-zip-runme-py-music-serpentine-plumbing-first-find-based-f1f1fddfe092