## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Solución
Con ayuda de wireshark y la llave que nos dan, hacemos uso de esta y nos da nuestra bandera
![[Pasted image 20240320121828.png]]
## Forma 2
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/webnet0$ ssldump -r capture.pcap -k picopico.key -d | grep pico -A3
    61 67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67    ag: picoCTF{nong
    73 68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63    shim.shrimp.crac
    6b 65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c    kers}..Content-L
    65 6e 67 74 68 3a 20 38 32 31 0d 0a 4b 65 65 70    ength: 821..Keep
--
    67 3a 20 70 69 63 6f 43 54 46 7b 6e 6f 6e 67 73    g: picoCTF{nongs
    68 69 6d 2e 73 68 72 69 6d 70 2e 63 72 61 63 6b    him.shrimp.crack
    65 72 73 7d 0d 0a 43 6f 6e 74 65 6e 74 2d 4c 65    ers}..Content-Le
    6e 67 74 68 3a 20 31 30 30 0d 0a 4b 65 65 70 2d    ngth: 100..Keep-
## Notas
