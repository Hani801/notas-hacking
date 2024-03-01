## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/14/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/14/level2.flag.txt.enc) in the same directory too.
## Solución
hani06@DESKTOP-4NE4RTQ:~$ wget https://artifacts.picoctf.net/c/14/level2.py
--2024-02-29 08:07:39--  https://artifacts.picoctf.net/c/14/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: ‘level2.py’

level2.py                     100%[=================================================>]     914  --.-KB/s    in 0s

2024-02-29 08:07:47 (2.43 MB/s) - ‘level2.py’ saved [914/914]

hani06@DESKTOP-4NE4RTQ:~$ wget https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
--2024-02-29 08:07:54--  https://artifacts.picoctf.net/c/14/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.26, 3.161.55.64, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: ‘level2.flag.txt.enc’

level2.flag.txt.enc           100%[=================================================>]      31  --.-KB/s    in 0s

2024-02-29 08:08:03 (571 KB/s) - ‘level2.flag.txt.enc’ saved [31/31]

hani06@DESKTOP-4NE4RTQ:~$ ls
codebook.txt  file       fixme2.pyM-D         level1.py            level2.py
code.py       fixme2.py  level1.flag.txt.enc  level2.flag.txt.enc  picosCTF
hani06@DESKTOP-4NE4RTQ:~$ vim level2.py

[1]+  Stopped                 vim level2.py
hani06@DESKTOP-4NE4RTQ:~$ python3 level2.py
Please enter correct password for flag: 521019957
That password is incorrect
hani06@DESKTOP-4NE4RTQ:~$ vim level2.py
hani06@DESKTOP-4NE4RTQ:~$ python3 level2.py
Please enter correct password for flag: 521019957
That password is incorrect
hani06@DESKTOP-4NE4RTQ:~$ vim level2.py
hani06@DESKTOP-4NE4RTQ:~$ python3 level2.py
Please enter correct password for flag: 4ec9
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_9701e681}
## Notas

## Referencias
