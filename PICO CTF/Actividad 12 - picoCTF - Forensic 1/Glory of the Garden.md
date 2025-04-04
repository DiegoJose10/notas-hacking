This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.
Hints:
- What is a hex editor?
# Solucion
Un **editor hexadecimal** (o **editor de archivos binarios**) es un tipo de programa informático que permite a un usuario modificar archivos binarios
Descargamos el archivo de garden usando wget y nos aparece que es un archivo .jpg y al abrirlo es una foto de un jardin.
Usando un editor hexadecimal como hexeditor podemos ver los caracteres hexadecimales y al buscar usando control+w y buscando como texto como buscar pico y de esa manera aparece la bandera.
O sino usando el comando strings garden.jpg podemos ver las cadenas que hay en el archivo binario de garden.jpg y hasta el final aparece la bandera o para mas facil usando el filtro de | grep pico podemos filtrar y ver la bandera mas facil
picoCTF{more_than_m33ts_the_3y3eBdBd2cc}
# Referencias
- https://es.wikipedia.org/wiki/Editor_hexadecimal
