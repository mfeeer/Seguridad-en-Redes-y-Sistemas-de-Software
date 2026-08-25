## Descripción
Do you know how to move between directories and read files in the shell? Start the container, `ssh` to it, and then `ls` once connected to begin.
## Solución

```
ssh` as `ctf-player` with the password, `8c606eb1` on the host `wily-courier.picoctf.net` and port `60418`
ssh ctf-player@wily-courier picoctf.net -p 60418 
ctf-player@pico-chall$ ls
1of3.flag.txt  instructions-to-2of3.txt
ctf-player@pico-chall$ cat lof3.flag.txt
cat: lof3.flag.txt: No such file or directory
ctf-player@pico-chall$ cat 1of3.flag.txt
picoCTF{xxsh_
ctf-player@pico-chall$ cat instructiones-to-2of3.txt
cat: instructiones-to-2of3.txt: No such file or directory
ctf-player@pico-chall$ cat instructions-to-2of3.txt
Next, go to the root of all things, more succinctly `/`
ctf-player@pico-chall$ cd /
ctf-player@pico-chall$ ls
2of3.flag.txt  bin  boot  challenge  dev  etc  home  instructions-to-3of3.txt  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
ctf-player@pico-chall$ cat 2of3.flag.txt
0ut_0f_//4t3r_
ctf-player@pico-chall$ cd
ctf-player@pico-chall$ ls
3of3.flag.txt  drop-in
ctf-player@pico-chall$ cat 3of3.flag.txt 
0b24fc4f}ctf-player@pico-chall$ 
```

## Notas adicionales
- **`cat 1of3.flag.txt`**
Muestra en pantalla el contenido del archivo especificado
- - **`cat 2of3.flag.txt`**
Lee la segunda parte de la bandera situada en la raíz 
    
- **`cat 3of3.flag.txt`**
Muestra la tercera y última parte de la bandera

## Referencias

`