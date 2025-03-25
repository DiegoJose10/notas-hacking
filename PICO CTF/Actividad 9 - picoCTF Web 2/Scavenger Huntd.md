There is some interesting information hidden around this site [http://mercury.picoctf.net:55079/](http://mercury.picoctf.net:55079/). Can you find it?
Hints:
- You should have enough hints to find the files, don't run a brute forcer.
# Solucion
La solucion de la bandera esta dividida en 5 partes:
- La primera parte esta al momento de inspeccionar el código fuente
- La segunda parte esta al momento de ver la hoja de estilos
- La tercera parte se encuentra viendo el archivo robots de la pagina: mercury.picoctf.net:55079/robots.txt 
- La cuarta parte esta viendo el archivo del servidor apache http de la pagina: http://mercury.picoctf.net:55079/.htaccess
- La quinta parte esta viendo el archivo desktop services stores de la pagina: http://mercury.picoctf.net:55079/.DS_Store
Uniendo las partes queda:
picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_74cceb07}
# Referencias

- https://httpd.apache.org/docs/2.4/es/howto/htaccess.html
- https://developers.google.com/search/docs/crawling-indexing/robots/intro?hl=es
- https://www.softzone.es/programas/sistema/ds_store/