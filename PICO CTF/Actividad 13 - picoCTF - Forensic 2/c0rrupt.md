We found this [file](https://jupiter.challenges.picoctf.org/static/ab30fcb7d47364b4190a7d3d40edb551/mystery). Recover the flag
Hints:
- Try fixing the file header
# Solucion
Usando el comando file lo reconocerá como data, pero inspeccionando el header con xxd -g 1 mystery | head podemos ver los strings que son comunes en los archivos PNG.  Por lo cual, se intentaran arreglar diversas strings para transformar el archivo en png, las cuales son:
- Cambiar los primeros 8 bytes del archivo para que sea reconocido en formato png: printf '\x89\x50\x4E\x47\x0D\x0A\x1A\x0A' | dd of=fixed.png bs=1 seek=0 count=8 conv=notrunc
- Cambiar el primer chunk a IHDR: printf '\x00\x00\x00\x0D\x49\x48\x44\x52' | dd of=fixed.png bs=1 seek=8 count=8 conv=notrunc
- Corregir el checksum: printf '\x00\x00' | dd of=fixed.png bs=1 seek=83 count=2 conv=notrunc
Usando pngcheck -v -f fixed.png podemos observar que ya no hay errores y al abrir la imagen aparece la bandera
picoCTF{c0rrupt10n_1847995}