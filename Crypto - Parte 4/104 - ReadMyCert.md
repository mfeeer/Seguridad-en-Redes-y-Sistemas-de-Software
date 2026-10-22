## Descripción

How about we take you on an adventure on exploring certificate signing requests Take a look at this CSR file [here](https://challenge-files.cylabacademy.net/library/5106e781bbd36dcc1335e6ad005b28467f171c07351768e71d06bf9cafb3c1f6/readmycert.csr).

pistas:

1. Download the certificate signing request and try to read it.
## Solución

```
Descargamos el archivo, una vez descargado ejecutamos estos comandos:

file readmycert.csr
openssl req -in readmycert.csr -noout -text

y buscamos la flag dentro de lo que nos arrojó:
academy{read_mycert_52274715}

```
## Notas adicionales
## Referencias
