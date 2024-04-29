## Objetivo
Can you get the flag? Download this [binary](https://artifacts.picoctf.net/c/87/gdbme). Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`
## Solución
![[Pasted image 20240429124203.png]]
## Notas
El programa tiene como problema un sleep, es decir que tenemos que esperar cierto tiempo para que nos de la bandera, pero con los comando que nos especifican nos "saltamos" esas especificaciones 