We found this [file](https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n). Recover the flag.
Hints:
- Weird that it won't display right...
# Solucion
Usando exiftool notamos que el archivo descargable es una imagen bitmap (bmp). La imagen no se muestra correctamente cuando la abrimos, asi que se debe corromper de alguna manera:
Usando HexEditor vemos que los primeros bytes del header del mapa de bits son:
```
42 4d 8e 26 2c 00 00 00 00 00 ba d0 00 00 ba d0
00 00 6e 04 00 00 32 01
```
Viendo como el número de bytes en el header están mal y el número de bits por píxel también ya que no coincide con un bmp, nos damos cuenta de que necesitamos editar los bytes en offset 0x0e y 0x1c. Los bytes correctos son los siguientes:
```
42 4d 8e 26 2c 00 00 00 00 00 ba d0 00 00 28 00
00 00 6e 04 00 00 40 03
```
Renombrando el archivo "tunn3lv1s10n" a "tunn3lv1s10n.bmp" se puede abrir y asi obtener la bandera.
picoCTF{qu1t3_a_v13w_2020}
