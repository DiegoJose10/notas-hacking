Download this image and find the flag. [Download image](https://artifacts.picoctf.net/c/216/pico.flag.png)
Hints:
- We know the end sequence of the message will be `$t3g0`.
# Solución
Usando zsteg en la imagen con el comando `zsteg pico.flag.png`muestra la bandera en la salida.
Zsteg es una herramienta para detectar esteganografía LSB en el caso de imágenes PNG y BMP

picoCTF{7h3r3_15_n0_5p00n_a1062667}