## Objetivo
Can you crack the password to get the flag? Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too. There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Solución
haniara-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py
--2024-03-01 15:36:56--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py           100%[==================>]   1.31K  --.-KB/s    in 0s      

2024-03-01 15:36:56 (69.9 MB/s) - 'level3.py' saved [1337/1337]

haniara-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2024-03-01 15:37:07--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc 100%[==================>]      31  --.-KB/s    in 0s      

2024-03-01 15:37:07 (1.37 MB/s) - 'level3.flag.txt.enc' saved [31/31]

haniara-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.hash.bin
--2024-03-01 15:37:17--  https://artifacts.picoctf.net/c/18/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin     100%[==================>]      16  --.-KB/s    in 0s      

2024-03-01 15:37:17 (410 KB/s) - 'level3.hash.bin' saved [16/16]

haniara-picoctf@webshell:~$ ls
README.txt    file                 level3.hash.bin  static
]             file.1               level3.py        static.ltdis.strings.txt
code.py       fixme1.py            ltdis.sh         static.ltdis.x86_64.txt
codebook.txt  flag                 nano.231.save    strings
convertme.py  level3.flag.txt.enc  nano.235.save    warm
haniara-picoctf@webshell:~$ vim level3.py 
haniara-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 8799
That password is incorrect
haniara-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: d3ab
That password is incorrect
haniara-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 1ea2
That password is incorrect
haniara-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: acaf
That password is incorrect
haniara-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}

## Notas

## Referencias
