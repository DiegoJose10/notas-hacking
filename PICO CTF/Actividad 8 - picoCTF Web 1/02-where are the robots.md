Can you find the robots? `https://jupiter.challenges.picoctf.org/problem/36474/` ([link](https://jupiter.challenges.picoctf.org/problem/36474/)) or http://jupiter.challenges.picoctf.org:36474

Hints:
- What part of the website could tell you where the creator doesn't want you to look?
# Solucion

Un archivo robots.txt indica a los rastreadores de los buscadores a qué URLs de tu sitio pueden acceder
Al sitio web le añadimos /robots.txt para ver el sitio al que no podemos acceder, despues nos aparece el mensaje del 
User-agent: *
Disallow: /477ce.html
Asi que a la pagina raiz le añadimos lo que tiene disallow y al entrar ahi aparece la bandera:
picoCTF{ca1cu1at1ng_Mach1n3s_477ce}
# Referencias

- https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es