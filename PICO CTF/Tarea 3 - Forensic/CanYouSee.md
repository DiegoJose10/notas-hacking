How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/131/unknown.zip).

Hints:
- How can you view the information about the picture?
- If something isn't in the expected form, maybe it deserves attention?
# Solución
Se descomprime el archivo usando unzip, vemos que tenemos una imagen, para analizar sus metadatos usamos exiftool ukn-reality.jpg y en la informacion vemos que en attribution url hay un codigo en base 64, usando cyberchef lo desciframos y vemos que esa es la bandera
picoCTF{ME74D47A_HIDD3N_d8c381fd}

# Referencias
- https://gchq.github.io/CyberChef/