## Descripción

Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/699d021acdedf3ce7c6944b6f3e16046a82b3a1f7ee2e79716132292ce4adbbd/disk.flag.img.gz)
## Solución
```

 wget https://challenge-files.cylabacademy.net/library/699d021acdedf3ce7c6944b6f3e16046a82b3a1f7ee2e79716132292ce4adbbd/disk.flag.img.gz
 
(Fer㉿Fersita)-[~/sleuthkitap]
└─$ fls -o 360448 -r 1995 disk.flag.img
Error stat(ing) image file (raw_open: image "1995" - No such file or directory)

┌──(Fer㉿Fersita)-[~/sleuthkitap]
└─$ fls -o 360448 -r disk.flag.img 1995
r/r 2363:       .ash_history
d/d 3981:       my_folder
+ r/r * 2082(realloc):  flag.txt
+ r/r 2371:     flag.uni.txt

┌──(Fer㉿Fersita)-[~/sleuthkitap]
└─$ icat -o 360448 disk.flag.img 2082
            3.449677            13.056403

┌──(Fer㉿Fersita)-[~/sleuthkitap]
└─$ icat -o 360448 disk.flag.img 2371
academy{by73_5urf3r_6395be48}
```

## Notas adicionales
## Referencias
