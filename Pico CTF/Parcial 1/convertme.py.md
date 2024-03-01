## Objetivo
Run the Python script and convert the given number from decimal to binary to get the flag. [Download Python script](https://artifacts.picoctf.net/c/23/convertme.py)

## Solución
haniara-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/23/convertme.py
--2024-02-29 01:06:04--  https://artifacts.picoctf.net/c/23/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py        100%[==================>]   1.16K  --.-KB/s    in 0s      

2024-02-29 01:06:04 (38.7 MB/s) - 'convertme.py' saved [1189/1189]

haniara-picoctf@webshell:~$ ls
README.txt    convertme.py  nano.231.save  static.ltdis.strings.txt
code.py       flag          nano.235.save  static.ltdis.x86_64.txt
codebook.txt  ltdis.sh      static         warm
haniara-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_7d102d7a}
haniara-picoctf@webshell:~$ cat codebook.txt 
azbycxdwevfugthsirjqkplomn
haniara-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_1a94e0f9}
haniara-picoctf@webshell:~$ pyhton3 convertme.py
-bash: pyhton3: command not found
haniara-picoctf@webshell:~$ python convertme.py
If 30 is in decimal base, what is it in binary base?
Answer: 11110
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_9c3b7d4d}
## Notas
## Referencias
