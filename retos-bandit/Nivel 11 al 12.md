## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel
Usuario: bandit11@bandit.labs.overthewire.org
Contraseña: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
Puerto: 2220
## Solución
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr "a-zA-Z" "n-za-mN-ZA-M"
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Notas
El rot13
## Referencias 
https://www.xataka.com/historia-tecnologica/asi-rot13-algoritmo-cifrado-simple-que-ha-revivido-para-ocultar-spoilers
