## Objetivo
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell. [Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
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
haniara-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2024-03-01 15:41:06--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py            100%[==================>]     270  --.-KB/s    in 0s      

2024-03-01 15:41:07 (138 MB/s) - 'runme.py' saved [270/270]

haniara-picoctf@webshell:~$ ls
README.txt    fixme1.py            nano.235.save
]             flag                 runme.py
code.py       level3.flag.txt.enc  static
codebook.txt  level3.hash.bin      static.ltdis.strings.txt
convertme.py  level3.py            static.ltdis.x86_64.txt
file          ltdis.sh             strings
file.1        nano.231.save        warm
haniara-picoctf@webshell:~$ python2 runme.py 
-bash: python2: command not found
haniara-picoctf@webshell:~$ python3 runme.py 
picoCTF{run_s4n1ty_run}

## Notas

## Referencias
