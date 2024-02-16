## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel
Usuario: bandit7@bandit.labs.overthewire.org
Contraseña: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
Puerto: 2220

## Solución
```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep millionth
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

## Notas adicionales
El comando grep sirve para hacer filtros de búsqueda
## Referencias
https://www.hostinger.es/tutoriales/comando-grep-linux

