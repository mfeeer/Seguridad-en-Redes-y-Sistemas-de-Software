## Descripción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.cylabacademy.net/library/c9d53b01e497af3b9886cf52c7896ec4b26d82dd88402905e13258cbbbe82b21/scrambled1.png) [scrambled2.png](https://challenge-files.cylabacademy.net/library/c9d53b01e497af3b9886cf52c7896ec4b26d82dd88402905e13258cbbbe82b21/scrambled2.png)

pistas:

[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)

2. Think of different ways you can "stack" images
## Solución

Usamos este script:
```python
import numpy as np
from PIL import Image

# Open images
im1 = Image.open("scrambled1.png")
im2 = Image.open("scrambled2.png")

# Make into Numpy arrays
im1np = np.array(im1)
im2np = np.array(im2)

# Add images
result = im2np + im1np
# Convert back to PIL image and save
Image.fromarray(result).save('result.png')


```
Encontramos la flag:
academy{2f16d0c4}


## Notas adicionales
## Referencias
