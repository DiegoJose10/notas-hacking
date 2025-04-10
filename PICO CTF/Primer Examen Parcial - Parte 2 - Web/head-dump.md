Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag. The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden. The website is running [picoCTF News](http://verbal-sleep.picoctf.net:63973/).
Hints:
- Explore backend development with us
- The head was dumped.
# Solucion
El reto nos lleva a un sitio web de blogs. Después de ver los sitios web, al final dando click en API Documentation nos lleva a **/api-docs,** que tiene Swagger, la cual es una herramienta para visualizar e interactuar con las API. Swagger reveló varias rutas de la API, en donde estaba el endpoint heapdump en la sección _Diagnosing_, la cual al darle clic en ejecutar nos daba un archivo .heapsnapshot, descargando este archivo ibamos a la terminal de linux y usando el comando cat heapdump-1744227027136.heapsnapshot | grep picoCTF{ nos suelta la bandera.
picoCTF{Pat!3nt_15_Th3_K3y_8635db4b}