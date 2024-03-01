## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?
## Solución
haniara-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
--2024-02-29 02:49:49--  https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings             100%[==================>] 757.84K  1.83MB/s    in 0.4s    

2024-02-29 02:49:50 (1.83 MB/s) - 'strings' saved [776032/776032]

haniara-picoctf@webshell:~$ ls
README.txt    convertme.py  flag           static                    warm
]             file          ltdis.sh       static.ltdis.strings.txt
code.py       file.1        nano.231.save  static.ltdis.x86_64.txt
codebook.txt  fixme1.py     nano.235.save  strings
haniara-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_827aee91}
## Notas
El comando “strings” es una herramienta muy útil en Linux que permite extraer cadenas de texto legibles de archivos binarios
## Referencias
