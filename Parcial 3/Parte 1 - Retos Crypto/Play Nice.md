## Objetivo
Not all ancient ciphers were so bad... The flag is not in standard format. `nc mercury.picoctf.net 21003` [playfair.py](https://mercury.picoctf.net/static/3329978ea3a249ef44d929b41afc5370/playfair.py)
## Solución
C:\Users\Hani>python -c "print('TKV5Z9ZPEHCLTKQFT47NY0HMNT5LTC'.lower())"
tkv5z9zpehcltkqft47ny0hmnt5ltc
C:\Users\Hani>ncat mercury.picoctf.net 21003
Here is the alphabet: 0uxtb3w4kj26q9m8gioe7nvahplr5dy1fzcs
Here is the encrypted message: xj5c181ropf5xjmyujnv0wlqrjdrbz
What is the plaintext message? tkv5z9zpehcltkqft47ny0hmnt5ltc
Congratulations! Here's the flag: 3f4b60ebf36369258d8638d2038c7ad1


## Notas
El cifrado Vigenère es un algoritmo de cifrado polialfabético inventado por el criptólogo francés Blaise de Vigenère en el siglo XVI. Se basa en un cifrado de turno al que se le agrega el uso de una palabra clave que cambia el turno en cada paso.