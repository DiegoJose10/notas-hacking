We have several pages hidden. Can you find the one with the flag? The website is running [here](http://saturn.picoctf.net:61640/).
Hints:
- folders folders folders
# Solucion
Si checamos el codigo fuente del sitio web encontramos que algunos de los archivos están en una carpeta llamada "secreto". Si navegamos hasta el suburl secreto (http://saturn.picoctf.net:54925/secret/), encontramos un sitio web diferente. Si repetimos el mismo proceso que antes, encontramos que hay otra carpeta llamada, hidden, por lo que navegamos a http://saturn.picoctf.net:54925/secret/hidden/. Seguimos repitiendo y vamos llegando a sitios web que nos acercan a la bandera. 
Al final la URL quedaria asi:
http://saturn.picoctf.net:61640/secret/hidden/superhidden/ y al inspeccionar el codigo fuente aparece la bandera:
picoCTF{succ3ss_@h3n1c@10n_790d2615}