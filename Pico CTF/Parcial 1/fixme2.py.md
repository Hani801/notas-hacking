## Objetivo
Fix the syntax error in the Python script to print the flag. [Download Python script](https://artifacts.picoctf.net/c/6/fixme2.py)
## Solución
hani06@DESKTOP-4NE4RTQ:~$ wget https://artifacts.picoctf.net/c/6/fixme2.py
--2024-02-29 07:43:02--  https://artifacts.picoctf.net/c/6/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.100, 3.161.55.26, 3.161.55.61, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.100|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: ‘fixme2.py’

fixme2.py                     100%[=================================================>]   1.00K  --.-KB/s    in 0s

2024-02-29 07:43:11 (2.78 MB/s) - ‘fixme2.py’ saved [1029/1029]

hani06@DESKTOP-4NE4RTQ:~$ ls
codebook.txt  code.py  file  fixme2.py  picosCTF
hani06@DESKTOP-4NE4RTQ:~$ nano fixme2.py
hani06@DESKTOP-4NE4RTQ:~$ ls
codebook.txt  code.py  file  fixme2.py  fixme2.pyM-D  picosCTF
hani06@DESKTOP-4NE4RTQ:~$ python3 fixme2.pyM-D
-bash: python3: command not found
hani06@DESKTOP-4NE4RTQ:~$ nano fixme2.py

hani06@DESKTOP-4NE4RTQ:~$ python3 fixme2.py
  File "/home/hani06/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
hani06@DESKTOP-4NE4RTQ:~$ nano fixme2.py
hani06@DESKTOP-4NE4RTQ:~$ python3 fixme2.py
  File "/home/hani06/fixme2.py", line 1
    =
    ^
SyntaxError: invalid syntax
hani06@DESKTOP-4NE4RTQ:~$ nano fixme2.py
hani06@DESKTOP-4NE4RTQ:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_f6a5aefc}
## Notas

## Referencias
