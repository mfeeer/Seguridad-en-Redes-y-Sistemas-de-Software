## Descripción

🥛 [http://xebec.cylabacademy.net:18816/](http://xebec.cylabacademy.net:18816/)


1. Look at the problem category
## Solución
 
```
descargamos la imagen 
wget http://chatelaine.cylabacademy.net:12169/concat_v.png

- extraer todos los datos ocultos
 zsteg -a concat_v.png
- filtramos la salida para encontrar la flag
 RUBY_THREAD_VM_STACK_SIZE=50000000 zsteg -a concat_v.png | grep aca
 academy{imag3_m4n1pul4t10n_sl4p5}
```
## Notas adicionales
## Referencias
