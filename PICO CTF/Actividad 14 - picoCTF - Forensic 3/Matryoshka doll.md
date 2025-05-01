Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/1b70cffdd2f05427fff97d13c496963f/dolls.jpg)
Hints:
- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}
# Solucion
El reto nos da un enlace para descargar una imagen llamada dolls.jpg. en la cual hay archivos ocultos dentro de este archivo. Para extraerlos usamos binwalk: binwalk -e dolls.jpg
Vemos un directorio llamado "base-images" en el que nos dirigimos y encontramos otro archivo de imagen llamado "2-c.jpg".
Intentamos de nuevo binwalk para extraer cualquier archivo oculto de esta imagen como tal y cambiamos nuestro directorio de trabajo a la de los archivos extraídos usando cd, el proceso se repite hasta que en los archivos encontremos flag,txt, la cual al usar cat en ella nos muestra la bandera
picoCTF{bf6acf878dcbd752f4721e41b1b1b66b}