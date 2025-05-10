Can you get the real meaning from this file. Download the file [here](https://artifacts.picoctf.net/c_titan/110/enc_flag).
Hints:
- Engaging in various decoding processes is of utmost importance
# Solución
Al descargar el archivo y abrirlo nos aparece:
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclh6ZzJhMnd6TW1zeWZRPT0nCg==
Usando cyberchef lo decodificamos y nos da:
b'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrXzg2a2wzMmsyfQ==
Quitando b' y volviendo a decodifcarlo nos da:
wpjvJAM{jhlzhy_k3jy9wa3k_86kl32k2}==
Ahora usando un decodificador online de codigo cesar lo decodificamos y nos da la bandera
picoCTF{caesar_d3cr9pt3d_86de32d2}

# Referencias
- https://gchq.github.io/CyberChef/
- https://www.dcode.fr/cifrado-cesar