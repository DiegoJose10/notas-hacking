Python scripts are invoked kind of like programs in the Terminal... Can you run [this Python script](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using [this password](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get [the flag](https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?
Hints:
- Get the Python script accessible in your shell by entering the following command in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py`
- `$ man python`
# Solucion
Usando wget descargamos los 3 archivos de la descripcion, usando cat en el archivo de python vemos que está construido para interactuar con un archivo llamado "pole.txt" y que soporta dos argumentos (-e/-d).  Mirando la función para el programa podemos ver cómo el programa decodificará el archivo. Así que cuando ejecutemos el programa cumpliremos este requisito, pero  pedira una contraseña, que esta en el archivo "pw.txt". Utilizando el `cp`copiaremos el archivo .flag.txt.en. y lo renombraremos a .pole.txt.
Ahora que tenemos el nombre de archivo correcto y entendemos cómo funciona el programa de python, podemos ejecutar `python3 ende.py -d pole.txt`para obtener la bandera. Cuando el programa pide la contraseña, sólo tenemos que copiar/pegar el contenido de .pw.txt y pulsar enter.

picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}