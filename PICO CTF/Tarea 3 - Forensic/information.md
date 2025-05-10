Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg)
Hints:
- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}
# Solución
Vemos que tenemos una imagen, para analizar sus metadatos usamos exiftool cat.jpg y en la informacion vemos que en license hay un codigo en base 64, usando cyberchef lo desciframos y vemos que esa es la bandera
picoCTF{the_m3tadata_1s_modified}

# Referencias
- https://gchq.github.io/CyberChef/