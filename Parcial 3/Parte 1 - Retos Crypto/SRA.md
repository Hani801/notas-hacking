## Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check... Connect to the program on our server: `nc saturn.picoctf.net 53987` Download the program: [chal.py](https://artifacts.picoctf.net/c/298/chal.py)
## Solución
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/SRA$ cat  chal.py
from Crypto.Util.number import getPrime, inverse, bytes_to_long
from string import ascii_letters, digits
from random import choice

pride = "".join(choice(ascii_letters + digits) for _ in range(16))
gluttony = getPrime(128)
greed = getPrime(128)
lust = gluttony * greed
sloth = 65537
envy = inverse(sloth, (gluttony - 1) * (greed - 1))

anger = pow(bytes_to_long(pride.encode()), sloth, lust)

print(f"{anger = }")
print(f"{envy = }")

print("vainglory?")
vainglory = input("> ").strip()

if vainglory == pride:
    print("Conquered!")
    with open("/challenge/flag.txt") as f:
        print(f.read())
else:
    print("Hubris!")
from Crypto.Util.number import isPrime, long_to_bytes
from string import ascii_letters, digits
from itertools import combinations
from sympy import divisors
from math import log2

anger = int(input("anger = "))
envy = int(input("envy = "))
sloth = 65537

ds = divisors(envy * sloth - 1)
primes = [x + 1 for x in ds if isPrime(x + 1)]
correct_size_primes = [x for x in primes if log2(x) // 1 == 127]

valid_plaintexts = []
charset = ascii_letters + digits
for p, q in combinations(correct_size_primes, 2):
    try:
        s = long_to_bytes(pow(anger, envy, p * q)).decode("ascii")
        if all([c in charset for c in s]):
            valid_plaintexts.append(s)
    except Exception:
        continue

print(valid_plaintexts)
C:\Users\Hani\Documents\picoCTF\SRA>python chal.py
anger = 36515363974813435099344355360944904535826225628716471235052504025786295887957
envy = 26963517300468693722773872408160148742203876732514988939711767509216849310293
['9PrmHmCy5Slq4Z64']

C:\Users\Hani>ncat saturn.picoctf.net 57282
anger = 36515363974813435099344355360944904535826225628716471235052504025786295887957
envy = 26963517300468693722773872408160148742203876732514988939711767509216849310293
vainglory?
> 9PrmHmCy5Slq4Z64
9PrmHmCy5Slq4Z64
Conquered!
picoCTF{7h053_51n5_4r3_n0_m0r3_b2f9b414}
## Notas

