## Objetivo
Fix the syntax error in this Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/25/fixme1.py)
## Solución
haniara-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/25/fixme1.py
--2024-02-29 02:30:37--  https://artifacts.picoctf.net/c/25/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.16, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py           100%[==================>]     837  --.-KB/s    in 0s      

2024-02-29 02:30:37 (32.6 MB/s) - 'fixme1.py' saved [837/837]

haniara-picoctf@webshell:~$ ls
README.txt    convertme.py  flag           static
]             file          ltdis.sh       static.ltdis.strings.txt
code.py       file.1        nano.231.save  static.ltdis.x86_64.txt
codebook.txt  fixme1.py     nano.235.save  warm
haniara-picoctf@webshell:~$ nano fixme1.py 
haniara-picoctf@webshell:~$ nano fixme1.py 
haniara-picoctf@webshell:~$ pyhton3 fixme1.py 
-bash: pyhton3: command not found
haniara-picoctf@webshell:~$ pyhton fixme1.py 
-bash: pyhton: command not found
haniara-picoctf@webshell:~$ python3 fixme1.py 
  File "/home/haniara-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
haniara-picoctf@webshell:~$ python fixme1.py 
  File "/home/haniara-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
haniara-picoctf@webshell:~$ python3 fixme1.py
  File "/home/haniara-picoctf/fixme1.py", line 20
    print('That is correct! Here\'s your flag: ' + flag)
IndentationError: unexpected indent
haniara-picoctf@webshell:~$ vim fixme1.py

[1]+  Stopped                 vim fixme1.py
haniara-picoctf@webshell:~$ nano fi
file       file.1     fixme1.py  
haniara-picoctf@webshell:~$ nano fixme1.py 
haniara-picoctf@webshell:~$ python3 fixme1.py
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_6a476c8f}
## Notas
## Referencias
