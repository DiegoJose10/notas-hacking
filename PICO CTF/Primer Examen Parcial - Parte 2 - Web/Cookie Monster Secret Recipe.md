Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe? You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:56241/) and good luck
Hints:
- Sometimes, the most important information is hidden in plain sight. Have you checked all parts of the webpage?
- Cookies aren't just for eating - they're also used in web technologies!
- Web browsers often have tools that can help you inspect various aspects of a webpage, including things you can't see directly.
# Solucion
Al entrar hacemos login con cualquier valor de usuario y contraseña y se genera una cookie, la cual usando cyberchef decodificandola desde base64 a url muestra la bandera
picoCTF{c00k1e_m0nster_l0ves_c00kies_6C2FB7F3}
# Referencias
- https://gchq.github.io/CyberChef/