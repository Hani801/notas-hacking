## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso al nivel
Usuario: bandit12@bandit.labs.overthewire.org
Contraseña: VNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
Puerto: 2220
## Solución
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txtx| zcat |file -
xxd: data.txtx: No such file or directory
gzip: stdin: unexpected end of file
/dev/stdin: empty
bandit12@bandit:~$ xxd -r data.txt| zcat |file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |tar xO | tar xO |file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |tar xO | tar xO |bzcat | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |tar xO | tar xO |bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Thu Oct  5 06:19:20 2023, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |tar xO | tar xO |bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt| zcat |bzcat | zcat |tar xO | tar xO |bzcat | tar xO |  zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
## Notas
xxd vaciado hexadecimal
## Referencias 
https://es.linux-console.net/?p=9702
