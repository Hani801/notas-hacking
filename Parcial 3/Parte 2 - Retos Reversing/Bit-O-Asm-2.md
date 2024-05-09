## Objetivo
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`. Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Solución
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/Bit-O-Asm-1$ cat disassembler-dump0_b.txt
<+0>:     endbr64
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret

picoCTF{654874}
## Notas
La bandera se obtiene sacando el número que tiene eax, en esta caso también hay un DWORD, es esencial saber algo de ensamblador, para saber que el numero que estamos buscando es 0x9fe1a, en decimal es 654874

