## Descripción

Download this disk image and find the flag.

Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://challenge-files.cylabacademy.net/library/7d645367284f9df9139dd5ad212e5c3bd0815b7674ca700648a3983158394892/disk.flag.img.gz)
## Solución

```
wget https://challenge-files.cylabacademy.net/library/7d645367284f9df9139dd5ad212e5c3bd0815b7674ca700648a3983158394892/disk.flag.img.gz
openssl aes256 -salt -in flag.txt -out flag.txt.enc -out flag.txt -k unbreakablepassword1234567 -d
Can't open "flag.txt" for reading, No such file or directory
409725FED07E0000:error:80000002:system library:BIO_new_file:No such file or directory:../crypto/bio/bss_file.c:67:calling fopen(flag.txt, rb)
409725FED07E0000:error:10000080:BIO routines:BIO_new_file:no such file:../crypto/bio/bss_file.c:75:

┌──(Fer㉿Fersita)-[~/sleuthkitap]
└─$ cat flag.txt
cat: flag.txt: No such file or directory

┌──(Fer㉿Fersita)-[~/sleuthkitap]
└─$ openssl enc -aes-256-cbc -d -salt -in flag.txt.enc -out flag.txt -k unbreakablepassword1234567
*** WARNING : deprecated key derivation used.
Using -iter or -pbkdf2 would be better.
bad decrypt
40F7EFDCDC710000:error:1C800064:Provider routines:ossl_cipher_unpadblock:bad decrypt:../providers/implementations/ciphers/ciphercommon_block.c:107:

┌──(Fer㉿Fersita)-[~/sleuthkitap]
└─$ cat flag.txt
academy{h4un71ng_p457_718ebd29}
```

## Notas adicionales
## Referencias
