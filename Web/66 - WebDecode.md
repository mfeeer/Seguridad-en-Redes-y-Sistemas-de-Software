
## Descripción

Do you know how to use the web inspector? Start searching [here](http://chatelaine.cylabacademy.net:31674/) to find the flag

pistas:

1. Use the web inspector on other files included by the web page.

2. The flag may or may not be encoded
## Solución
- para este reto entramos al link de la pagina proporcionada, una vez dentro checamos las pestañas de la página, en la cual podemos encontrar que en about nos dice que podemos intentar inspeccionando el código. 
- Al inspeccionarlo pudimos encontrar este atributo con base64 notify_true="YWNhZGVteXt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMDc5ODliMjV9
- Por lo que acudimos a cyberchef para poder desencriptar el mensaje y con ellos pudimos encontrar la flag correspondiente:
academy{web_succ3ssfully_d3c0ded_07989b25}
## Notas adicionales
## Referencias
https://gchq.github.io/CyberChef/