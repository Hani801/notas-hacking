## Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Solución
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/webnet1$ ls -latotal 96
drwxrwxrwx 1 hani06 hani06  4096 Mar 20 12:23 .
drwxrwxrwx 1 hani06 hani06  4096 Mar 20 12:22 ..
-rwxrwxrwx 1 hani06 hani06 92525 Oct 26  2020 capture.pcap
-rwxrwxrwx 1 hani06 hani06  1704 Oct 26  2020 picopico.key
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/webnet1$ ls
capture.pcap  picopico.key  vulture.jpg
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/webnet1$ strings -n 10 vulture.jpg | grep pico
picoCTF{honey.roasted.peanuts}


## Notas
