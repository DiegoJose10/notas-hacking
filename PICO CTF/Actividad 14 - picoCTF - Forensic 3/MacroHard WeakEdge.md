I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics is fun.pptm)
# Solucion
Un archivo de PowerPoint se puede extraer y ver su contenido usando binwalk.
Por lo cual primero extraemos la presentación de PowerPoint como archivo ZIP: unzip Forensics\ is\ fun.pptm
Despues miramos a través de los archivos extraídos, en los cuales aparece: ppt/slideMasters/hidden
Luego, leyendo ese archivo: cat ppt/slideMasters/hidden muestra un codigo en base 64: `Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q`.
Finalmente, lo decodificamos usando [CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64\('A-Za-z0-9%2B/%3D',true\)&input=WiBtIHggaCBaIHogbyBnIGMgRyBsIGogYiAwIE4gVSBSIG4gdCBFIE0gVyBSIGYgZCBWIDkgciBiIGogQiAzIFggMyBCIHcgZCBIIE4gZiBjIGwgOSA2IE0gWCBBIDEgZiBR) para conseguir la bandera.
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
# Referencias
- https://gchq.github.io/CyberChef/


