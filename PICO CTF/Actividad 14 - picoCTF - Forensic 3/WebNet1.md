We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
Hints:
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?
# Solucion
El pcap que nos proporcionan es una conexión TLS con datos encriptados, la mayoría de los protocolos y conjuntos de cifrado TLS están bien encriptados y sin la clave privada no podemos desencriptar los datos, pero en este reto tenemos la clave privada, asi que solo hay que desencriptarlo, pero en este caso hay que unir la salida hacia el archivo, para eso usamos el comando: ssldump -r capture.pcap -k picopico.key -d > output
Ahora abriendo el archivo en un editor de texto y y usando Ctrl+f  buscamos picoCTF, habra muchas banderas falsas, asi que seguiremos buscando hasta encontrar la bandera verdadera:
picoCTF{honey.roasted.peanuts}