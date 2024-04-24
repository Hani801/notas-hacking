## Objetivo
What does asm3(0xd2c26416,0xe6cf51f0,0xe54409d5) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/df999527eaecf46f259c4337a820856c/test.S)
## Solución
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/asm$ cat test.S.2
asm3:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0x9]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xe]
        <+15>:  add    ah,BYTE PTR [ebp+0xf]
        <+18>:  xor    ax,WORD PTR [ebp+0x12]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret
|   |   |   |   |   |
|---|---|---|---|---|
|EAX|0x00000375||EBX|0x00000000|
|ECX|0x00000000||EDX|0x00000000|
|ESI|0x00000000||EDI|0x00000000|
|EBP|0x00000000||ESP|0x000203F0|
|EIP|0x00020438|Ln 16, Col 9|   |   

Bandera: 0x375

## Notas
Con ayuda de un emulador, compilamos el programa
