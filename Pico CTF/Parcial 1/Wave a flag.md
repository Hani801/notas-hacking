## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
## Solución
haniara-picoctf@webshell:~$ ls
README.txt  flag  warm
haniara-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
haniara-picoctf@webshell:~$ chmod +x warm
haniara-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
haniara-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
## Notas

## Referencias
