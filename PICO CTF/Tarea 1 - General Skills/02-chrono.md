How to automate tasks to run at intervals on linux servers? Use ssh to connect to this server:

```
Server: saturn.picoctf.net
Port: 52668
Username: picoplayer 
Password: kZx-HVJKu8
```
# Solucion
Se conecta  a la cuenta indicada en la descripcion y nos movemos al directorio raiz de la cuenta y usamos la barra invertida \ y entramos a la carpeta etc y leemos el archivo crontab en el cual esta la bandera
```
diegojfh1000-picoctf@webshell:~$ ssh picoplayer@saturn.picoctf.net -p 52668     
The authenticity of host '[saturn.picoctf.net]:52668 ([13.59.203.175]:52668)' can't be established.
ED25519 key fingerprint is SHA256:dMTscRrUiURy7uMu5eGWwEKdd2FzqLzx6LfWhssWnNQ.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:9: [hashed name]
    ~/.ssh/known_hosts:11: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:52668' (ED25519) to the list of known hosts.
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.5 LTS (GNU/Linux 6.5.0-1023-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

This system has been minimized by removing packages and content that are
not required on a system that users do not log into.

To restore this content, you can run the 'unminimize' command.

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ ls
picoplayer@challenge:~$ cd ..
picoplayer@challenge:/home$ ls 
picoplayer
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ \
> 
picoplayer@challenge:/$ cat /etc/crontab
# picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}
```
picoCTF{Sch3DUL7NG_T45K3_L1NUX_5b7059d0}