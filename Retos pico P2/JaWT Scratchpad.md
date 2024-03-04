## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/63090/` or http://jupiter.challenges.picoctf.org:63090

## Solución
# Logged in!

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Desktop$ hashcat -m 16500 crack rockyou.txt
hashcat (v6.2.6) starting

OpenCL API (OpenCL 3.0 PoCL 3.1+debian  Linux, None+Asserts, RELOC, SPIR, LLVM 15.0.6, SLEEF, DISTRO, POCL_DEBUG) - Platform #1 [The pocl project]
==================================================================================================================================================
* Device #1: pthread-haswell-AMD Ryzen 5 3450U with Radeon Vega Mobile Gfx, 2229/4522 MB (1024 MB allocatable), 8MCU

Minimum password length supported by kernel: 0
Maximum password length supported by kernel: 256

Hashes: 1 digests; 1 unique digests, 1 unique salts
Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
Rules: 1

Optimizers applied:
* Zero-Byte
* Not-Iterated
* Single-Hash
* Single-Salt

Watchdog: Hardware monitoring interface not found on your system.
Watchdog: Temperature abort trigger disabled.

Host memory required for this attack: 2 MB

Dictionary cache built:
* Filename..: rockyou.txt
* Passwords.: 14344391
* Bytes.....: 139921497
* Keyspace..: 14344384
* Runtime...: 2 secs

eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiSGFuaSJ9.L-5PFJ37i7MNmDFIQAgGZjs2aPvI7zgChNI2baKXBvo:ilovepico

Session..........: hashcat
Status...........: Cracked
Hash.Mode........: 16500 (JWT (JSON Web Token))
Hash.Target......: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiSG...aKXBvo
Time.Started.....: Mon Mar  4 13:16:11 2024 (6 secs)
Time.Estimated...: Mon Mar  4 13:16:17 2024 (0 secs)
Kernel.Feature...: Pure Kernel
Guess.Base.......: File (rockyou.txt)
Guess.Queue......: 1/1 (100.00%)
Speed.#1.........:  1234.1 kH/s (1.83ms) @ Accel:512 Loops:1 Thr:1 Vec:8
Recovered........: 1/1 (100.00%) Digests (total), 1/1 (100.00%) Digests (new)
Progress.........: 7397376/14344384 (51.57%)
Rejected.........: 0/7397376 (0.00%)
Restore.Point....: 7393280/14344384 (51.54%)
Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
Candidate.Engine.: Device Generator
Candidates.#1....: iloverober2117* -> ilovemymum55

Started: Mon Mar  4 13:15:04 2024
Stopped: Mon Mar  4 13:16:18 2024
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Desktop$ hashcat -m 16500 crack rockyou.txt --show
eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoiSGFuaSJ9.L-5PFJ37i7MNmDFIQAgGZjs2aPvI7zgChNI2baKXBvo:ilovepico

## Notas
