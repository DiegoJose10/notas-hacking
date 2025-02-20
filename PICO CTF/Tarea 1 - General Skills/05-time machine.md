What was I last working on? I remember writing a note to help me remember... You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/161/challenge.zip)
Hints
- The `cat` command will let you read a file, but that won't help you here!
- Read the chapter on Git from the picoPrimer [here](https://primer.picoctf.org/#_git_version_control).
- When committing a file with git, a message can (and should) be included.
# Solucion
Se descarga el archivo, se descomprime, luego entramos a la carpeta de drop-in, despues usamos los comandos de git init para empezar cambios de git,  y git log para ver la informacion y ahi aparece la bandera
```
diegojfh1000-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c_titan/161/challenge.zip
--2025-02-20 00:20:08--  https://artifacts.picoctf.net/c_titan/161/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17739 (17K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip                                              100%[=======================================================================================================================================>]  17.32K  --.-KB/s    in 0.006s  

2025-02-20 00:20:08 (2.87 MB/s) - 'challenge.zip' saved [17739/17739]

diegojfh1000-picoctf@webshell:~$ ls
README.txt  challenge.zip
diegojfh1000-picoctf@webshell:~$ unzip challenge.zip
Archive:  challenge.zip
   creating: drop-in/
  inflating: drop-in/message.txt     
   creating: drop-in/.git/
   creating: drop-in/.git/branches/
  inflating: drop-in/.git/description  
   creating: drop-in/.git/hooks/
  inflating: drop-in/.git/hooks/applypatch-msg.sample  
  inflating: drop-in/.git/hooks/commit-msg.sample  
  inflating: drop-in/.git/hooks/fsmonitor-watchman.sample  
  inflating: drop-in/.git/hooks/post-update.sample  
  inflating: drop-in/.git/hooks/pre-applypatch.sample  
  inflating: drop-in/.git/hooks/pre-commit.sample  
  inflating: drop-in/.git/hooks/pre-merge-commit.sample  
  inflating: drop-in/.git/hooks/pre-push.sample  
  inflating: drop-in/.git/hooks/pre-rebase.sample  
  inflating: drop-in/.git/hooks/pre-receive.sample  
  inflating: drop-in/.git/hooks/prepare-commit-msg.sample  
  inflating: drop-in/.git/hooks/update.sample  
   creating: drop-in/.git/info/
  inflating: drop-in/.git/info/exclude  
   creating: drop-in/.git/refs/
   creating: drop-in/.git/refs/heads/
 extracting: drop-in/.git/refs/heads/master  
   creating: drop-in/.git/refs/tags/
 extracting: drop-in/.git/HEAD       
  inflating: drop-in/.git/config     
   creating: drop-in/.git/objects/
   creating: drop-in/.git/objects/pack/
   creating: drop-in/.git/objects/info/
   creating: drop-in/.git/objects/43/
 extracting: drop-in/.git/objects/43/246218ab4fc7b30e9a9dff073e012316851469  
   creating: drop-in/.git/objects/25/
 extracting: drop-in/.git/objects/25/16effb8d70e33bdd0023629b164a77225e1ec2  
   creating: drop-in/.git/objects/10/
 extracting: drop-in/.git/objects/10/228f3d6437701ef5aaac04213757031f30ebec  
  inflating: drop-in/.git/index      
 extracting: drop-in/.git/COMMIT_EDITMSG  
   creating: drop-in/.git/logs/
  inflating: drop-in/.git/logs/HEAD  
   creating: drop-in/.git/logs/refs/
   creating: drop-in/.git/logs/refs/heads/
  inflating: drop-in/.git/logs/refs/heads/master  
diegojfh1000-picoctf@webshell:~$ ls 
README.txt  challenge.zip  drop-in
diegojfh1000-picoctf@webshell:~$ cd drop-in
diegojfh1000-picoctf@webshell:~/drop-in$ ls -la
total 4
drwxr-xr-x 3 diegojfh1000-picoctf diegojfh1000-picoctf  37 Mar 12  2024 .
drwxr-xr-x 3 diegojfh1000-picoctf diegojfh1000-picoctf  91 Feb 20 00:20 ..
drwxr-xr-x 8 diegojfh1000-picoctf diegojfh1000-picoctf 166 Mar 12  2024 .git
-rw-r--r-- 1 diegojfh1000-picoctf diegojfh1000-picoctf  87 Mar 12  2024 message.txt
diegojfh1000-picoctf@webshell:~/drop-in$ git init
Reinitialized existing Git repository in /home/diegojfh1000-picoctf/drop-in/.git/
diegojfh1000-picoctf@webshell:~/drop-in$ git log
```
```
Usando git log
commit 10228f3d6437701ef5aaac04213757031f30ebec (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:24 2024 +0000

    picoCTF{t1m3m@ch1n3_8defe16a}
```

picoCTF{t1m3m@ch1n3_8defe16a}