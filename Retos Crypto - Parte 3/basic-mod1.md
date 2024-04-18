## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme. Download the message [here](https://artifacts.picoctf.net/c/127/message.txt). Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore. Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
## Solución
datos = open("message.txt").read().split()
#print(trype(datos))
#print(datos)
flag = ""
c = ""
for n in datos:
        i = int(n) % 37
        if i >= 0 and i <= 25:
                c = chr(i + 65)
        elif i >= 26 and i <= 35:
                c = chr(i + 22)
        elif i == 36:
                c = "_"
        flag = flag + c
print(flag)
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF$ python3 exp.py
R0UND_N_R0UND_79C18FB3
Bandera: picoCTF{R0UND_N_R0UND_79C18FB3}
## Notas
