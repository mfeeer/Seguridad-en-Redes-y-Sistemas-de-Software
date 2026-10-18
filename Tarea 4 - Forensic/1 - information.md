## Descripción
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg)

pistas:

1. Look at the details of the file

2. Make sure to submit the flag as academy{XXXXX}
## Solución
```
- Descargamos el archivo
wget https://challenge-files.cylabacademy.net/library/c585b4adbdaa06f409db7bf5012c2e58e9aab24669764a5f1cf0f9ce0d60dcfd/cat.jpg
- abrimos el archivo para ver su contenido
 open cat.jpg

- inspeccionamos los metadatos del archivo
Fer@Fersita:~$ exiftool cat.jpg

- decodificamos la cadena de base 64
 echo "YWNhZGVteXt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d

- encontramos la flag:
academy{the_m3tadata_1s_modified}
```
## Notas adicionales
## Referencias
