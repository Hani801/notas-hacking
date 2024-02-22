## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de acceso al nivel
Usuario: bandit10@bandit.labs.overthewire.org
Contraseña: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
Puerto: 2220
## Solución
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
## Notas
Base64 es un tipo de codificado 
## Referencias 
https://developer.mozilla.org/es/docs/Glossary/Base64
