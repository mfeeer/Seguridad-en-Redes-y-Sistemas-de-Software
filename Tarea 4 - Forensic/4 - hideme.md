## Descripción
Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://challenge-files.cylabacademy.net/library/072ab2768814bc12f4cc180b5e7bf48e8501774bfb741ff9263792824887fd04/flag.png).
## Solución
```
para este reto utilizamos:
 binwalk flag.png.1
 
una vez viendo el archivo oculto
binwalk -e flag.png.1
entramos y obtenemos la flag:
academy{Hiddinng_An_imag3_within_@n_ima9e_ba7f84d1}
```
## Notas adicionales
## Referencias