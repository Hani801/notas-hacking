## Objetivo
Can you get the flag? Here's the [website](http://saturn.picoctf.net:58179/). We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Solución
flag.txt esta por encima de ciertas carpetas por lo que se usó: `../../../../../flag.txt`
Bandera: picoCTF{7h3_p47h_70_5ucc355_6db46514}
## Notas

## Referencias