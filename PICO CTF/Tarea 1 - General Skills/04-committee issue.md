I accidentally wrote the flag down. Good thing I deleted it! You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/137/challenge.zip)
Hints
- Version control can help you recover files if you change or lose them!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control)
- You can 'checkout' commits to see the files inside them

# Solucion
Se descarga el archivo, se descomprime, luego entramos a la carpeta de drop-in, despues usamos los comandos de git init para empezar cambios de git, git log para ver la informacion y git checkout para crear la bandera, finalmente usamos cat para leer el contenido de message.txt y ver la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/137/challenge.zip
--2025-02-20 00:12:08--  https://artifacts.picoctf.net/c_titan/137/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19197 (19K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[=======================================================================================================================================>]  18.75K  --.-KB/s    in 0.008s  

2025-02-20 00:12:08 (2.35 MB/s) - 'challenge.zip' saved [19197/19197]

diegojfh1000-picoctf@webshell:~$ unzip challenge.zip
diegojfh1000-picoctf@webshell:~$ cd drop-in
diegojfh1000-picoctf@webshell:~/drop-in$ ls -la
total 4
drwxr-xr-x 3 diegojfh1000-picoctf diegojfh1000-picoctf  37 Feb 20 00:12 .
drwxr-xr-x 3 diegojfh1000-picoctf diegojfh1000-picoctf  60 Feb 20 00:12 ..
drwxr-xr-x 8 diegojfh1000-picoctf diegojfh1000-picoctf 166 Feb 20 00:12 .git
-rw-r--r-- 1 diegojfh1000-picoctf diegojfh1000-picoctf  11 Mar 12  2024 message.txt
diegojfh1000-picoctf@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/diegojfh1000-picoctf/drop-in/.git/
diegojfh1000-picoctf@webshell:~/drop-in$ git log

diegojfh1000-picoctf@webshell:~/drop-in$ git checkout ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0
Note: switching to 'ea859bf3b5d94ee74ce5ee1afa3edd7d4d6b35f0'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at ea859bf create flag
diegojfh1000-picoctf@webshell:~/drop-in$ cat message.txt
picoCTF{s@n1t1z3_cf09a485}
```
picoCTF{s@n1t1z3_cf09a485}