Do you know how to use the web inspector? Start searching [here](http://titan.picoctf.net:55893/) to find the flag
Hints:
- Use the web inspector on other files included by the web page.
- The flag may or may not be encoded
# Solucion
Navegando en el sitio web vemos que en el codigo html de la pagina de about hay una pista que esta codificada: cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZjZmNmI3OGF9 
Y al decodificarla usando cyberchef nos da la bandera: 
picoCTF{web_succ3ssfully_d3c0ded_f6f6b78a}
# Referencias
- https://gchq.github.io/CyberChef/
