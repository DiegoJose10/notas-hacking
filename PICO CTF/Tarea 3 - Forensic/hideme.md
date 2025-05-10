Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/256/flag.png).
# Solución
Se descarga el archivo, se usa hexeditor en el para analizarlo, se observa que la imagen es un archivo zip, usamos unzip para descomprimirlo y nos da una carpeta llamada secret, la cual contiene flag.png y al abrirla aparece la bandera.
picoCTF{Hiddinng_An_imag3_within_@n_ima9e_85e04ab8}