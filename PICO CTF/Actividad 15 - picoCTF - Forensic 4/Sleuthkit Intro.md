Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory. [Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz) Access checker program: `nc saturn.picoctf.net 52704`
# Solución
Se usa mmls disk.img para ver  la dirección offset para cada partición en la imagen y despues al conectarnos al servidor usando nc saturn.picoctf.net 52704 nos pregunta ¿Cuál es el tamaño de la partición de Linux en la imagen de disco dada? Nosotros al obtener ese dato usando mmls en la imagen del disco lo respondemos y asi nos suelta la bandera
picoCTF{mm15_f7w!}


