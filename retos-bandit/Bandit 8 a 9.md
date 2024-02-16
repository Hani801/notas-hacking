## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel
Usuario: bandit8@bandit.labs.overthewire.org
Contraseña: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
Puerto: 2220

## Solución
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
 1001  1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Notas adicionales
El comando sort es para ordenar líneas de archivos de texto
## Referencias
https://www.ibidemgroup.com/edu/tutorial-sort-linux-unix/

