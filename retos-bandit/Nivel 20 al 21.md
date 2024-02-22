## Objetivo
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
## Datos de acceso al nivel
Usuario: bandit20@bandit.labs.overthewire.org
Contraseña: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Puerto: 2220
## Solución
bandit20@bandit:~$ nc -lnvp 2548 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Listening on 0.0.0.0 2548
^C
bandit20@bandit:~$ nc -lnvp 2548 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3064863
bandit20@bandit:~$ Listening on 0.0.0.0 2548

bandit20@bandit:~$ jobs
[1]+  Running                 nc -lnvp 2548 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
bandit20@bandit:~$ fg
nc -lnvp 2548 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
^C
bandit20@bandit:~$ jobs
bandit20@bandit:~$ nc -lnvp 2548 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3067310
bandit20@bandit:~$ Listening on 0.0.0.0 2548
./suconnect 6678
Could not connect
bandit20@bandit:~$ ./suconnect 2548
Connection received on 127.0.0.1 53804
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq

## Notas

## Referencias 
