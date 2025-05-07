Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image: [dds1-alpine.flag.img.gz](https://mercury.picoctf.net/static/a734f18939e0aaea9d27bc7a243a0ed0/dds1-alpine.flag.img.gz)
Hints:
- Have you ever used `file` to determine what a file was?
- Relevant terminal-fu in picoGym: https://play.picoctf.org/practice/challenge/85
- Mastering this terminal-fu would enable you to find the flag in a single command: https://play.picoctf.org/practice/challenge/48
- Using your own computer, you could use qemu to boot from this disk!
# Solución
Después de descargar la imagen, se usa `gunzip`para descomprimirlo y luego se usa lo que dicec la descripción lo cual seria: `srch_strings`, pero como la salida es muy grande se usa ```
srch_strings dds1-alpine.flag.img | grep pico  
Asi nos aparecen las strings que contienen pico y en las cuales aparece la bandera
picoCTF{f0r3ns1c4t0r_n30phyt3_a69a712c} 