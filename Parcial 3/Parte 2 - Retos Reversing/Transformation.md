## Objetivo
I wonder what this really is... [enc](https://mercury.picoctf.net/static/77a2b202236aa741e988581e78d277a6/enc) `''.join([chr((ord(flag[i]) << 8) + ord(flag[i + 1])) for i in range(0, len(flag), 2)])`
## Solución
texto = '灩捯䍔䙻ㄶ形楴獟楮獴㌴摟潦弸強㕤㐸㤸扽'
flag = ''
for i in range(len(texto)):
    flag += chr(ord(texto[i]) >> 8)
    flag += chr(ord(texto[i]) - (ord(flag[-1]) << 8))

print(flag)

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/Transformation$ python3 flag.py
picoCTF{16_bits_inst34d_of_8_75d4898b}
## Notas
Con ayuda del código que nos dan, fue posible encontrar la bandera
