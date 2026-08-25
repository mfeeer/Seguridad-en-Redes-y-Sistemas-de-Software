## Descripción
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

Connect with nc fickle-tempest.picoctf.net 57524

pistas: 
1. I hear python can convert things.

2. It might help to have multiple windows open.
## Solución
```
Fers-academy@webshell:~$ nc fickle-tempest.picoctf.net 57524
Let us see how data is stored
chair
Please give the 01100011 01101000 01100001 01101001 01110010 as a word.

you have 45 seconds.....

Input:
chair
Please give me the  o154 o151 o172 o141 o162 o144 as a word.
Input:
lizard
Please give me the 6c697a617264 as a word.
Input:
lizard
You've beaten the challenge
picoCTF{learning_about_converting_values_563BAF26}
```


## Notas adicionales
- convertimos un numero binario a texto
- luego un numero octal a texto
- un hexadecimal a texto
- obtenemos la resolución del reto
## Referencias
https://gchq.github.io/CyberChef/