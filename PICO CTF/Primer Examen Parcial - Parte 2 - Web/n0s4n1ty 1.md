A developer has added profile picture upload functionality to a website. However, the implementation is flawed, and it presents an opportunity for you. Your mission, should you choose to accept it, is to navigate to the provided web page and locate the file upload area. Your ultimate goal is to find the hidden flag located in the `/root` directory. You can access the web application [here](http://standard-pizzas.picoctf.net:53620/)!
Hints:
- File upload was not sanitized
- Whenever you get a shell on a remote machine, check `sudo -l`
# Solucion
Abriendo el sitio web y viendo el codigo fuente se puede observar que cualquier tipo de script puede ser subido, asi que se crea una webshell.php y se sube para asi tener acceso al servidor y podemos notar que desde el url podemos generar comandos que seran activados por el servidor. Finalmente entrando a http://standard-pizzas.picoctf.net:53620/uploads/shell.php?cmd=sudo cat /root/flag.txt nos muestra la bandera
picoCTF{wh47_c4n_u_d0_wPHP_712a9451}