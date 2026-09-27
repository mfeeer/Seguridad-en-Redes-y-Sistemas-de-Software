
## Descripción

The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://chatelaine.cylabacademy.net:33952/) out.
## Solución
- para este reto damos click en el enlace proporcionado
- el reto nos propone ir a robots.txt el cual nos arroja esto:
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```
- podemos ver que tenemos un texto en base 64, que podemos desencriptar con cyberchef
- nos da una dirección js/myfile.txt la cual contiene la flag correspondiente:
academy{Who_D03sN7_L1k5_90B0T5_662b27d3}
## Notas adicionales
## Referencias
https://toolbox.itsec.tamu.edu/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=CmFuTXZiWGxtYVd4bExuUjRkQT09
