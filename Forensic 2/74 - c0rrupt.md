## Descripción


## Solución

```
sudo apt install pngcheck
```

Con esta, ya podremos revisar la integridad de nuestros archivos png, ahora, para nuestro caso nos iremos directamente a corregir los valores de nuestro archivo. Debemos de establecer correctamente los nombres de cada chunk con el fin que se vaya la corrupción de nuestro archivo png.

```
pngcheck -v mystery
open mystery
y obtenemos nuestra flag 
```
## Notas adicionales
## Referencias