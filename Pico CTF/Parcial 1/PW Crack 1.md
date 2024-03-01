## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
## Solución
hani06@DESKTOP-4NE4RTQ:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2024-02-29 07:59:40--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.26, 3.161.55.61, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.26|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: ‘level1.py’

level1.py                     100%[=================================================>]     876  --.-KB/s    in 0s

2024-02-29 07:59:55 (1.72 MB/s) - ‘level1.py’ saved [876/876]

hani06@DESKTOP-4NE4RTQ:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2024-02-29 08:00:15--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.100, 3.161.55.26, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: ‘level1.flag.txt.enc’

level1.flag.txt.enc           100%[=================================================>]      30  --.-KB/s    in 0s

2024-02-29 08:00:23 (5.02 MB/s) - ‘level1.flag.txt.enc’ saved [30/30]

hani06@DESKTOP-4NE4RTQ:~$ vim level1.py
hani06@DESKTOP-4NE4RTQ:~$ python3 level1.py
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
## Notas

## Referencias
