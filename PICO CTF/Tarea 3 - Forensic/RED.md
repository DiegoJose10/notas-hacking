RED, RED, RED, RED Download the image: [red.png](https://challenge-files.picoctf.net/c_verbal_sleep/831307718b34193b288dde31e557484876fb84978b5818e2627e453a54aa9ba6/red.png)
Hints:
- The picture seems pure, but is it though?
- Red?Ged?Bed?Aed?
- Check whatever Facebook is called now.
# Solución
Se descarga la imagen y se usa el comando zsteg -a red.png, **zsteg** es una herramienta utilizada para **la detección de estaganografía** en **imágenes de PNG y BMP**. zsteg **analiza** esencialmente **imágenes** para detectar **datos ocultos** (esteganografía). Y es capaz de extraer información oculta de **LSB (Least Significant Bit)** y otras **técnicas esteganográficas**. Al hacerlo dentro de la informacion aparece un codigo en base 64, el cual al decodificarlo usando cyberchef muestra la bandera.
picoCTF{r3d_1s_th3_ult1m4t3_cur3_f0r_54dn355_}

# Referencias
- https://gchq.github.io/CyberChef/