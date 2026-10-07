## Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.cylabacademy.net/library/84dbba88e43a94f37b661ea65f77bd65a746cd68e25aff9abefbcf780f48fcc2/dds1-alpine.flag.img.gz)

1. Have you ever used `file` to determine what a file was?

2. Relevant terminal-fu in Challenge Library: [https://learn.cylabacademy.org/library/85](https://learn.cylabacademy.org/library/85)

3. Mastering this terminal-fu would enable you to find the flag in a single command: [https://learn.cylabacademy.org/library/48](https://learn.cylabacademy.org/library/48)

4. Using your own computer, you could use qemu to boot from this disk!
## Solución
```
- descargamos el archivo
wget https://challenge-files.cylabacademy.net/library/84dbba88e43a94f37b661ea65f77bd65a746cd68e25aff9abefbcf780f48fcc2/dds1-alpine.flag.img.gz
-descomprime el archivo .gz
gzip -d dds1-alpine.flag.img.gz
- Examina la estructura del archivo descomprimido para **determinar su formato real
file dds1-alpine.flag.img

- indica que el archivo `dds1-alpine.flag.img` es una **imagen de disco cruda (raw image)** con una tabla de particiones **DOS/MBR**
dds1-alpine.flag.img: DOS/MBR boot sector; partition 1 : ID=0x83, active, start-CHS (0x0,32,33), end-CHS (0x10,81,1), startsector 2048, 260096 sectors

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ open dds1-alpine.flag.img
-encontramos la flag
┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ srch_strings dds1-alpine.flag.img | grep academy
academy{f0r3ns1c4t0r_n30phyt3_6502313d}
```


## Notas adicionales
## Referencias
