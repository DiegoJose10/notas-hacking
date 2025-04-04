We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
Hints:
- Try using a tool like Wireshark
- What are streams?
# Solucion
**PCAP** , acrónimo de **Captura de Paquetes** , es un formato de archivo ampliamente utilizado en el ámbito de las redes para almacenar datos capturados del tráfico de red. Un archivo PCAP contiene los datos sin procesar de los paquetes de red, incluidos los encabezados y las cargas útiles, lo que permite un examen exhaustivo de todas las comunicaciones que ocurren en una red. Estos archivos se suelen procesar mediante herramientas de captura de paquetes como Wireshark, tcpdump u otro software de monitorización de red. Una vez capturados, los datos se pueden analizar para diagnosticar problemas de conectividad, supervisar el rendimiento o investigar actividades sospechosas.
Se descarga la captura de paquetes usando wget, al identificarlo es un archivo .pcap
Usando Wireshark, abriendo ese archivo y analizandolo, le podemos dar clic a cualquier secuencia UDP, y siguiendo la transmision de datos en cada secuencia, se puede observar que en la secuencia 6 esta la bandera
picoCTF{StaT31355_636f6e6e}

# Referencias
-- https://www-comparitech-com.translate.goog/net-admin/pcap-guide/?_x_tr_sl=en&_x_tr_tl=es&_x_tr_hl=es&_x_tr_pto=tc