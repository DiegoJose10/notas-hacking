We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag
# Solucion
La solución esta en filtrar solo los protocolos UDP con el puerto 22. Todos los paquetes tienen los mismos datos, pero el primero y el último que contienen "inicio" y "fin" son **sospechosos**. Si no están en el cuerpo de los paquetes, sino en los encabezados, se revisa el encabezado UDP: ![UDP header](https://i.imgur.com/yaqSO9B.png)El puerto de destino es el mismo (22), al igual que la longitud, cada mensaje tiene un puerto de origen diferente. Cada uno empieza por 5 y tiene 3 dígitos. Los 3 dígitos son un código ASCII para caracteres y se debe ordenar segun la columna "Número": ![Columna de Núm.](https://i.imgur.com/n3NNcuO.png)E ingresando todos los números de nuevo y decodificándolos con cyberchef se puede obtener la bandera
 112 105 99 99 111 67 84 70 70 123 112 49 76 76 76 102 51 111 111 111 100 95 95 97 96 95 95 81 49 95 115 116 11 51 103 - 125
 picoCTF{p1LLf3r3d_data_v1a_st3g0
# Referencias
- https://gchq.github.io/CyberChef/
