There's something in the [building](https://jupiter.challenges.picoctf.org/static/011955b303f293d60c8116e6a4c5c84f/buildings.png). Can you retrieve the flag?
Hints:
- There is data encoded somewhere... there might be an online decoder.
# Solucion
Descargamos el archivo de building usando wget y al abrirlo es una foto de un edificio.
La estenografia es una forma de ocultar informacion sensitiva dentro de un archivo ordinario.
Usando stenography online, cargamos la imagen y le damos que la decodifique y al decodificarla nos aparece la bandera.
Tambien otra forma es usar zsteg, la cual es una herramienta dentro de la terminal que nos ayuda de igual forma que stenography online.
picoCTF{h1d1ng_1n_th3_b1t5}
# Referencias
- https://stylesuxx.github.io/steganography/
