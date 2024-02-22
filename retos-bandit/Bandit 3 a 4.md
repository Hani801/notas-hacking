## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de acceso al nivel
Usuario: bandit3@bandit.labs.overthewire.org
Contraseña: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
Puerto: 2220

## Solución
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$

```

## Notas adicionales
No tenía conocimiento del -a que con ese comando se pueden ver archivos ocultos
## Referencias
