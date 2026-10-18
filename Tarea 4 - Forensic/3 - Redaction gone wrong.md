## Descripción
Now you DON’T see me. This [report](https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a27705e2c94103/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?

pistas:

1. How can you be sure of the redaction?
## Solución
```

- descargamos el archivo
wget https://challenge-files.cylabacademy.net/library/455e6e9581a9272cf0cd6a8f2da0a7cdcfefdb52dc7a7f9c09a
27705e2c94103/Financial_Report_for_ABC_Labs.pdf
- extraemos el texto
pdftotext Financial_Report_for_ABC_Labs.pdf.1 salida.txt
 cat salida.txt
 
-obtenemos la flag
academy{C4n_Y0u_S33_m3_fully}
```
## Notas adicionales
## Referencias