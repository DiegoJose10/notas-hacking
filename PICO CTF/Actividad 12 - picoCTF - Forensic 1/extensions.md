This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
Hints:
- How do operating systems know what kind of file it is? (It's not just the ending!
- Make sure to submit the flag as picoCTF{XXXXX}
# Solucion
Todos los archivos tienen un formato, el cual es una forma estandar en que la informacion es coficada y almacenada en un archivo de computadora. En la cabecera de los archivos se usan magic bytes, los cuales identifican el tipo de archivo que es.
Usamos wget para descargar el archivo txt y nos damos cuenta que tiene extension .txt pero tiene cabecera de archivo png, por lo cual usando el comando mv flag.txt flag.png le cambiamos la extension al archivo de .txt a .png y lo abrimos usando open flag.png y asi aparece la bandera
picoCTF{now_you_know_about_extensions}

