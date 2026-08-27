## Descripción
Find the flag in the Python script!

[Download Python script](https://artifacts.picoctf.net/c/35/serpentine.py)

pistas:

1. Try running the script and see what happens

2. In the webshell, try examining the script with a text editor like `nano`

3. To exit `nano`, press Ctrl and x and follow the on-screen prompts.

4. The `str_xor` function does not need to be reverse engineered for this challenge.
## Solución
```
Fers-academy@webshell:~$ wget https://artifacts.picoctf.net/c/35/serpentine.py
Fers-academy@webshell:~$ nano serpentine.py
Fers-academy@webshell:~$ python3 serpentine.py

    Y
  .-^-.
 /     \      .- ~ ~ -.
()     ()    /   _ _   `.                     _ _ _
 \_   _/    /  /     \   \                . ~  _ _  ~ .
   | |     /  /       \   \             .' .~       ~-. `.
   | |    /  /         )   )           /  /             `.`.
   \ \_ _/  /         /   /           /  /                `'
    \_ _ _.'         /   /           (  (
                    /   /             \  \
                   /   /               \  \
                  /   /                 )  )
                 (   (                 /  /
                  `.  `.             .'  /
                    `.   ~ - - - - ~   .'
                       ~ . _ _ _ _ . ~

Welcome to the serpentine encourager!


a) Print encouragement
b) Print flag
c) Quit

What would you like to do? (a/b/c) b
picoCTF{7h3_r04d_l355_7r4v3l3d_ae0b80bd}


cambiamos el bloque elif que tenía por esto:
 elif choice == 'b':
      print_flag()
      print("adios!")
      sys.exit(0)
esto permite que la bandera se imprima correctamente
```
## Notas adicionales

## Referencias