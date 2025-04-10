Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer. `ssh -p 55076 ctf-player@saturn.picoctf.net`. The password is `3f39b042`
Hints:
- What programs do you have access to?
# Solucion
Al entrar a la instancia nos vamos metiendo en diferentes directorios y leyendo el contenido de los archivos para ver donde esta la bandera para eso usamos los comandos cd y echo $(<nombre del archivo), para encontrar la bandera usamos cd ctfplayer/ cd ala y echo $(<kazam.txt).
picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}