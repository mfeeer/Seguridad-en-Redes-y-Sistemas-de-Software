## Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

[Download disk image](https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz)

## Solución

```
wget https://challenge-files.cylabacademy.net/library/d8718cbbc14dcd9f9aad532a51d7a01b00e1715ca3b1d654dfef687d0b15cbf5/disk.img.gz

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ gzip -d disk.img.gz

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ ls .lah
ls: cannot access '.lah': No such file or directory

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ ls -lah
total 229M
drwxr-xr-x  2 Fer Fer 4.0K Oct  7 11:10 .
drwx------ 20 Fer Fer 4.0K Oct  7 10:57 ..
-rw-r--r--  1 Fer Fer 128M Sep 22 20:21 dds1-alpine.flag.img
-rw-r--r--  1 Fer Fer 100M Sep 22 20:52 disk.img

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ mmls disk.img
DOS Partition Table
Offset Sector: 0
Units are in 512-byte sectors

      Slot      Start        End          Length       Description
000:  Meta      0000000000   0000000000   0000000001   Primary Table (#0)
001:  -------   0000000000   0000002047   0000002048   Unallocated
002:  000:000   0000002048   0000204799   0000202752   Linux (0x83)

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ nc xebec.cylabacademy.net 31475
What is the size of the Linux partition in the given disk image?
Length in sectors:                                                                                              |0000202752
                                                                                                |0000202752
This script encountered an error. Did you input a regular decimal number?

┌──(Fer㉿Fersita)-[~/diskdisksleuth]
└─$ nc xebec.cylabacademy.net 31475
What is the size of the Linux partition in the given disk image?
Length in sectors: 202752
202752
Great work!
academy{mm15_f7w!}
```
## Notas adicionales
## Referencias
