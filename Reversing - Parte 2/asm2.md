## Objetivo
What does asm2(0x4,0x21) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/7e3eb2f90200ac88126f62ceb4bc3948/test.S)
## Solución
asm2:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   sub    esp,0x10
        <+6>:   mov    eax,DWORD PTR [ebp+0xc]
        <+9>:   mov    DWORD PTR [ebp-0x4],eax
        <+12>:  mov    eax,DWORD PTR [ebp+0x8]
        <+15>:  mov    DWORD PTR [ebp-0x8],eax
        <+18>:  jmp    0x509 <asm2+28>
        <+20>:  add    DWORD PTR [ebp-0x4],0x1
        <+24>:  add    DWORD PTR [ebp-0x8],0x74
        <+28>:  cmp    DWORD PTR [ebp-0x8],0xfb46
        <+35>:  jle    0x501 <asm2+20>
        <+37>:  mov    eax,DWORD PTR [ebp-0x4]
        <+40>:  leave
        <+41>:  ret

>>> 0xfb46
64326
>>> 74
74
>>> 0x74
116
>>> 0xfb46 / 0x74
554.5344827586207
>>> 0x21
33
>>> hex(33 + 555)
'0x24c'
## Notas
