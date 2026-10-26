## Descripción

This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://challenge-files.cylabacademy.net/library/765fe2e27bfd01f2fc3432d711fedd1ef1103879d9bfff0302de118737fa4d0c/VaultDoor4.java)

pistas:

1. Use a search engine to find an "ASCII table"

2. You will also need to know the difference between octal, decimal, and hexadecimal numbers.
## Solución

```python
python3 -c "print(''.join([chr(x) for x in [106, 85, 53, 116, 95, 52, 95, 98, 0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f, 0o142, 0o131, 0o164, 0o63, 0o163, 0o137, 0o142, 0o64]] ) + 'e943c3a0')"


#academy{jU5t_4_bUnCh_0f_bYt3s_136aaf3703}
```
## Notas adicionales
## Referencias
