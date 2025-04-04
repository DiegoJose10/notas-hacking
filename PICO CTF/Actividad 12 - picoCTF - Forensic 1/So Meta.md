Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).
Hints:
- What does meta mean in the context of files?
- Ever heard of metadata?
# Solucion
Los metadatos son datos que proporcionan informacion de otros datos, pero no su contenido, por ejemplo el texto de un mensaje o una imagen en si misma o una ficha de un libro en una biblioteca, ayuda al usuario a descubirir informacion relevante y administrar recursos.
Descargamos el archivo usando wget y usamos la herramienta exiftool para ver la ficha o informacion del archivo y podemos observar que la bandera esta en la informacion del artista del archivo
picoCTF{s0_m3ta_d8944929}