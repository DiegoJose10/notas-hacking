Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm) has extraordinarily helpful information...
Hints:
- This program will only work in the webshell or another Linux computer.
- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm`
- Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`
- -h and --help are the most common arguments to give to programs to get more information from them!
- Not every program implements help features like -h and --help.
# Solucion
Se usa wget para descargar el archivo, el archivo se llama warm, luego se verifica que este con ls, despues se ejecuta con ./, hubo un permiso denegado, asi que se usa chmod +x para poder obtener el permiso, luego al ejecutarlo nos dice que usemos -h, un comando para mostrar la ayuda, y al usarlo junto con la ejecucion del archivo ya nos muestra la bandera.

```
diegojfh1000-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
--2025-02-17 23:13:21--  https://mercury.picoctf.net/static/a14be2648c73e3cda5fc8490a2f476af/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                  100%[=======================>]  10.68K  --.-KB/s    in 0s      

2025-02-17 23:13:21 (128 MB/s) - 'warm' saved [10936/10936]

diegojfh1000-picoctf@webshell:~$ ls
README.txt  file  flag  salida  strings  strings.1  warm
diegojfh1000-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
diegojfh1000-picoctf@webshell:~$ chmod +x warm
diegojfh1000-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
diegojfh1000-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_755f3544}
```
picoCTF{b1scu1ts_4nd_gr4vy_755f3544}