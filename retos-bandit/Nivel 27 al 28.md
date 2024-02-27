## Objetivo
There is a git repository at `ssh://bandit27-git@localhost/home/bandit27-git/repo` via the port `2220`. The password for the user `bandit27-git` is the same as for the user `bandit27`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel
Usuario: bandit27@bandit.labs.overthewire.org
Contraseña: YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
Puerto: 2220
## Solución
bandit27@bandit:~$ mkdir -p /tmp/secttp
bandit27@bandit:~$ cd /tmp/secttp
bandit27@bandit:/tmp/secttp$ git clone ssh://bandit27-git@localhost/home/bandit27-git/repo
fatal: destination path 'repo' already exists and is not an empty directory.
bandit27@bandit:/tmp/secttp$ git clone ssh://bandit27-git@localhost/home/bandit27-git/repo
fatal: destination path 'repo' already exists and is not an empty directory.
bandit27@bandit:/tmp/secttp$ ls -al repo
total 16
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 26 19:40 .
drwxrwxr-x 3 bandit27 bandit27 4096 Feb 26 19:40 ..
drwxrwxr-x 8 bandit27 bandit27 4096 Feb 26 19:40 .git
-rw-rw-r-- 1 bandit27 bandit27   68 Feb 26 19:40 README
bandit27@bandit:/tmp/secttp$ cat repo/README
The password to the next level is: AVanL161y9rsbcJIsFHuw35rjaOM19nR

## Notas
Se entró a un repositorio

## Referencias 
