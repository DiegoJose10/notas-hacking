Can you login to this website? Try to login [here](http://saturn.picoctf.net:59567/).
Hints: 
- `admin` is the user you want to login as.
# Solucion
En el sitio web hay un inicio de sesion con usuario y contraseña, asi que usamos la inyección SQL `' OR 1=1--`como contraseña o como usuario y  obtenemos una nueva pagina.
Ahora, observando su código fuente, tenemos la bandera
picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}