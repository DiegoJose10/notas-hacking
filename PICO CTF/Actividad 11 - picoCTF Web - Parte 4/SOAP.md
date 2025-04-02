The web project was rushed and no security assessment was done. Can you read the /etc/passwd file? [Web Portal](http://saturn.picoctf.net:53821/)

Hints:
- XML external entity Injection
# Solucion
La inyección de entidad externa XML (también conocida como XXE) es una vulnerabilidad de seguridad web que permite a un atacante interferir con el procesamiento de datos XML de una aplicación. A menudo permite a un atacante ver archivos en el sistema de archivos del servidor de aplicaciones, e interactuar con cualquier sistema de back-end o externo al que la propia aplicación pueda acceder.

En algunas situaciones, un atacante puede escalar un ataque XXE para comprometer el servidor subyacente u otra infraestructura de back-end, aprovechando la vulnerabilidad XXE para realizar ataques de falsificación de solicitud del lado del servidor (SSRF).

Encontramos la etiqueta `XXE` -> `XML external entity` y también al inspeccionar el sitio web podemos notar la relacion a xxe y en index.html vemos la ubicacion para la solicitud POST
Asi que ahora necesitamos hacer una solicitud POST a http://saturn.picoctf.net:53821/data with carga XML para obtener la bandera, para eso editar y reenviamos la solicitud en la red usando POST en vez de GET y editando el cuerpo de la solicitud para que de una carga XML:

~~~<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE data[ <!ENTITY file SYSTEM "file:///etc/passwd"> ]>
<data><ID>&file;</ID></data>
~~~

picoCTF{XML_3xtern@l_3nt1t1ty_e79a75d4}
# Referencias
- https://portswigger.net/web-security/xxe