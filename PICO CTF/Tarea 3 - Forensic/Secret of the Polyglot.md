The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file? Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/7/flag2of2-final.pdf).
Hints:
- This problem can be solved by just opening the file in different ways
# Solución
Al abrir el archivo nos muestra un pdf con la parte 2 de la bandera y al analizarlo usando hexeditor vemos que el archivo tiene un header de png, asi que al cambiar la extension a .png nos muestra la primera parte de la bandera, uniendo las partes tenemos la bandera completa.
`picoCTF{f1u3n7_1n_pn9_&_pdf_53b741d6}