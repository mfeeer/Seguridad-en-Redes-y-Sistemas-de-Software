## Descripción
How about trying to match a regular expression

The website is running [here](http://saturn.picoctf.net:58670/).
Access the webpage and try to match the regular expression associated with the text field
## Solución
  
```
Para este reto tenemos que ver el código fuente del link que nos proporcionan, en donde podemos ver  la expresión regular: ^p.....F!? la cual nos dice que debe de haber una p minúscula al inicio de la palabra, con al menos 5 caracteres cualquiera y una F al final de la palabra. Al introducir una como picoCTF nos da la flag correspondiente.
picoCTF{succ3ssfully_matchtheregex_2375af79}
```

## Notas adicionales
- usamos regexr para resolver este reto
## Referencias
https://regexr.com/
