## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.
## Solución
  GNU nano 7.2                                             exp.py                                                       d= open ("rev_this").read()
flag = ""

for j in range (8,23):
        if j & 1 == 0:
                flag += chr( ord(d[j]) - 5)
        else :
                flag += chr( ord(d[j]) + 2)
print(flag)

## Notas
Con ayuda de hidra, fue posible ver el código del problema y descubrir que 