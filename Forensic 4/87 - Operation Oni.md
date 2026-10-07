## Descripción
Download this disk image, find the key and log into the remote machine.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download disk image](https://challenge-files.cylabacademy.net/library/8af34b0fa863a6efa03d28278ca270b335291ad998f21c3696889bdc9c77ab72/disk.img.gz)
- Remote machine: `ssh -i key_file -p 17630 ctf-player@chatelaine.cylabacademy.net`
## Solución

```
-descargamos el archivo
 wget https://challenge-files.cylabacademy.net/library/8af34b0fa863a6efa03d28278ca270b335291ad998f21c3696889bdc9c77ab72/disk.img.gz
 
Extraer la clave privada
icat -o 206848 disk.img 2345 > key_file
- cambiar permisos del archivo
  chmod 600 key_file
- nos conectamos por ssh
ssh -i key_file -p 16967 ctf-player@chatelaine.cylabacademy.net

-leemos la bandera
cat flag.txt
-obtenemos la bandera correspondiente:
academy{k3y_5l3u7h_0e000cd7}
```

## Notas adicionales
## Referencias