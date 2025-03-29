The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:57618/) out.
# Solucion
Al entrar al sitio web usando /robots.txt en la despues de la pagina raiz vemos un codigo que sugiere que está en base 64. Sin embargo, si intentamos decodificarlo con un decodificador en línea, parece que la base 64 está ligeramente mal formada. Como el texto en base 64 ocupa tres líneas, al decodificar cada línea por separado, observamos que la segunda línea proporciona una ruta: js/myfile.txt. Si navegamos a la suburl, obtenemos la bandera:
picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}
# Referencias
- https://gchq.github.io/CyberChef/