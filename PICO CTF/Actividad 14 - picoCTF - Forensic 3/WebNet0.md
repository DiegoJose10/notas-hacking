We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
Hints:
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?
# Solucion
El pcap que nos proporcionan es una conexión TLS con datos encriptados, la mayoría de los protocolos y conjuntos de cifrado TLS están bien encriptados y sin la clave privada no podemos desencriptar los datos, pero en este reto tenemos la clave privada, asi que solo hay que descifrarlo, para eso usamos el comando: ssldump -r capture.pcap -k picopico.key -d
Y al mirar el resultado y desplazarse un poco hacia abajo aparece la bandera.
picoCTF{nongshim.shrimp.crackers}`