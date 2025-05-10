A group of underground hackers might be using this legit site to communicate. Use your forensic techniques to uncover their message Try it [here](http://standard-pizzas.picoctf.net:59286/)!
Hints:
- In the country that doesn't exist, the flag persists
# Solución
Al abrirlo nos muestra una pagina web con imagenes de banderas, inspeccionando el codigo fuente vemos que hay una bandera con codigo muy diferente a las demas, la cual es upanzi, descargamos la imagen de upanzi y en la terminal de linux usamos la herramienta de stepic. Stepic es un módulo Python y una herramienta de línea de comandos para ocultar datos arbitrarios dentro de imágenes modificando ligeramente los colores. Usamos el comando stepic -d -i upaz.png y nos muestra la bandera. 

picoCTF{fl4g_h45_fl4g6f5548ea}