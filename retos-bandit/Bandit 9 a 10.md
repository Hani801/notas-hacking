## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel
Usuario: bandit9@bandit.labs.overthewire.org
Contraseña: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
Puerto: 2220

## Solución
```
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
x]T========== theG)"
========== passwordk^
========== is
========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```

## Notas adicionales

## Referencias


