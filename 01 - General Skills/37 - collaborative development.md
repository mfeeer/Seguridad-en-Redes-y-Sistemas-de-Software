## Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?

You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/178/challenge.zip)
## Solución
```
Fers-academy@webshell:~/drop-in/drop-in$ wget https://artifacts.picoctf.net/c_titan/70/challenge.zip
Fers-academy@webshell:~/drop-in/drop-in$ unzip challenge.zip
Fers-academy@webshell:~/drop-in/drop-in$ cd drop-in
Fers-academy@webshell:~/drop-in/drop-in$ git config --global user.email "Fer"
Fers-academy@webshell:~/drop-in/drop-in$ git config --global user.email "Mendez"
Fers-academy@webshell:~/drop-in/drop-in$ git merge feature/part-1
Fers-academy@webshell:~/drop-in/drop-in$ git merge feature/part-2
Fers-academy@webshell:~/drop-in/drop-in$ nano flag.py
Fers-academy@webshell:~/drop-in/drop-in$ git commit -a
Fers-academy@webshell:~/drop-in/drop-in$ git merge feature/part-3
Fers-academy@webshell:~/drop-in/drop-in$ nano flag.py
Fers-academy@webshell:~/drop-in/drop-in$ git commit -a
Fers-academy@webshell:~/drop-in/drop-in$ python3 flag.py
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_6c06cec1}
```
## Notas adicionales
- En cada `nano flag.py` se corrige el archivo, esto se logra borrando el `>>>>> HEAD`, `=====` y `<<<<<< branch`
## Referencias