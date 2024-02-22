## Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de acceso al nivel
Usuario: bandit0@bandit.labs.overthewire.org
Puerto: 2220
Contraseña: bandit0

## Solución
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
bandit0@bandit:~$

## Notas adicionales
No se tenía conocimiento del comando cat readme por lo que se tuvo que hacer una investigación
## Referencias
https://man7.org/linux/man-pages/man1/cat.1.html




