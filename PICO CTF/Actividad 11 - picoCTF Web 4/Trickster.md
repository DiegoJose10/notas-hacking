I found a web app that can help process images: PNG images only! Try it [here](http://atlas.picoctf.net:59352/)!

# Solucion
Al entrar al sitio web nos pide subir un archivo png.
Revisando /robots.txt nos lleva a /instructions.txt y ahi podemos averiguar que el sitio web valida que las imagenes enviadas sean png y que sea una imagen, esto verificando que los archivos sea .png y que al principio el contenido del archivo sea PNG y podemos ver que el archivo subido se guardará en /uploads/.archivo. Conociendo esto, se crea un archivo  de webshell simple que pueda generar una interfaz de línea de comandos para que se ejecuten comandos en el servidor de forma remota. Antes de eso, tenemos que cumplir con los requisitos para subir el archivo. El servidor sólo comprueba los primeros caracteres para ser **PNG,** así que se los ponemos al principio del código y se añade extensión **.png** renombrando el archivo a **webshell.png.php** para que el script PHP disfrazara como una imagen de PNG.
Luego vamos a /uploads/webshell.png.php y obtenemos una interfaz de comando-línea para ejecutar comandos. A partir de este punto, podemos buscar la bandera en el sistema como queramos, la cual se encuentra usando cat /var/www/html/MRFDAZLDMUYDG.txt
picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_73198bd9} 
# Referencias
- https://gist.github.com/joswr1ght/22f40787de19d80d110b37fb79ac3985