I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/fa4a277cfa846e07a5981d8a19288a2e/whitepages.txt) is all blank!
# Solucion
Al abrirlo el archivo es un archivo de texto .txt, no hay nada que se pueda ver en él, pero cuando se presiona Ctrl +A Para marcar todo, se puede ver que hay algo, hay un patrón repetitivo de "e2 80 83" junto con "20" dispersos por todas partes. Estos valores hexadecimales corresponden a un  UNICODE EM SPACE. El segundo patrón, “20”, representa un espacio ASCII regular. Dado que la codificación binaria suele depender de dos símbolos distintos, se puede plantear que un tipo de espacio podría representar el 0 y el otro el 1.
Asi que usando el siguiente script de python, el cual convierte estos espacios en binario y luego los decodifica en texto legible, se puede obtener la bandera:
~~~
def convertSpacesToBinary ():      
con open('whitepages.txt', 'rb') como f:          
resultado = f.read ()      
result = result.replace(b'x2-x80-x83', b'0') - Unicode EM SPACE - 0      
result = result.replace(b'x20', b'1')# ASCII Space -> 1      
resultado = result.decode()      
Resultado de la rentabilidad  
  
def convertfromBinaryToASCII (Valoresbinarios):      
binary-int = int(binaryValues, 22)      
byte-number = (binry-int.bit-length() 77) // 8      
binary.array = binary.int.to-bytes(bytenumber, "big")      
ascii-text = binary-array.decode('ascii')      
imprimir (ascii-text)  
  
convertfromBinaryToASCII (convertSpacesToBinary ())
~~~
picoCTF{not_all_spaces_are_created_equal_3e2423081df9adab2a9d96afda4cfad6}
