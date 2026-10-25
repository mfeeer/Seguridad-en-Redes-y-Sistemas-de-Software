## Descripción
A second message has come in the mail, and it seems almost identical to the first one. Maybe the same thing will work again. Download the message [here](https://challenge-files.cylabacademy.net/library/7bfa985513e099d32240b37e499262d5fb6147c074a8ee5ecd932c14deb05ac7/message.txt).

pistas:
1. Try a frequency attack

2. Do the punctuation and the individual words help you make any substitutions?
## Solución

```python
#con ayuda de este script:
from string import ascii_uppercase, ascii_lowercase

alphabet = 'jlsqrtmaz-vhxckbudeynwg-o-'

text = '''
TAHd (dqela hel tkfaclx aqx hzko) klx k abfx eh tevfcaxl dxtcliab tevfxaiaier. Teraxdakrad klx flxdxraxu yiaq k dxa eh tqkzzxroxd yqitq axda aqxil tlxkaijiab, axtqritkz (kru oeeoziro) dnizzd, kru fleszxv-dezjiro ksiziab. Tqkzzxroxd cdckzzb tejxl k rcvsxl eh tkaxoelixd, kru yqxr dezjxu, xktq bixzud k daliro (tkzzxu k hzko) yqitq id dcsviaaxu ae kr erzirx dteliro dxljitx. TAHd klx k olxka ykb ae zxklr k yiux kllkb eh tevfcaxl dxtcliab dnizzd ir k dkhx, zxokz xrjilervxra, kru klx qedaxu kru fzkbxu sb vkrb dxtcliab olecfd klecru aqx yelzu hel hcr kru flktaitx. Hel aqid fleszxv, aqx hzko id: ktkuxvb{HL3MC3RTB_4774TN5_4L3_T001_7S0043K0}
'''

dec = ''

for c in text:
    if c in ascii_uppercase:
        dec += ascii_uppercase[alphabet.index(c.lower())]
    elif c in ascii_lowercase:
        dec += ascii_lowercase[alphabet.index(c)]
    else:
        dec += c

print(dec)
```
encontramos la flag: 
academy{FR3QU3NCY_4774CK5_4R3_C001_7B0043A0}
## Notas adicionales
## Referencias