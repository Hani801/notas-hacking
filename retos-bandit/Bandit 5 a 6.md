## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

## Datos de acceso al nivel
Usuario: bandit5@bandit.labs.overthewire.org
Contraseña: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
Puerto: 2220

## Solución
```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls -a
.            maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
..           maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
bandit5@bandit:~/inhere$ find . -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Notas adicionales
El comando find es utilizado para encontrar cosas y se le puede especificar el tamaño 
## Referencias
https://www.ionos.es/digitalguide/servidores/configuracion/comando-linux-find/
