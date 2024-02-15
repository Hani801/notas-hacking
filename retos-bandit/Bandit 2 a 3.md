## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso al nivel
Usuario: bandit2@bandit.labs.overthewire.org
Contraseña: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
Puerto: 2220

## Solución
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat
^C
bandit2@bandit:~$ cat spaces^C
bandit2@bandit:~$ ^C
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

```

## Notas adicionales

## Referencias
