## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso al nivel
Usuario: bandit15@bandit.labs.overthewire.org
Contraseña: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Puerto: 2220
## Solución
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 18 10:54:16 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 18 10:54:16 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 18 10:53:16 2024 GMT; NotAfter: Feb 18 10:54:16 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEcjY6OTANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjE4MTA1MzE2WhcNMjQwMjE4MTA1NDE2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCz
TX1NLedZhpQfXiWbWWD2BlNYjANpj+TnzUOI9ZbKJnOQJAbFfWZLA6No7XOStgje
+RPIoAHrX42G95VDfWtRms+qCsCTlUaS9291dZJQ3iOjBIE+PvmRcGdUlFJXDYa6
E61L2DKLbb8YSAnSuUPG3K7CtdxJpA5DpCBCmHEA9t5gZ5HGo9Gt9Kay9lhApX78
ocytwwHG15LplXI6LQB3ykhyCAcfljR3azd90T83dz7kLyM7yIMt60k1kemuX6RW
qSvkCvxmckRFoQPjwKZUopGLlhcC58Kb2xlwEGK+9j/ibBRkmEdBkOOeb5pJol7K
Wkd9LdG0nTWrggni7EKbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCA
j53OECoyjZMkHINZj35xk2kKQc9Jj9XjoCE0HlooUWd1ETik/2TkIbdWenozDrgH
10Jqmu/zAEhQkfFALBXCR7Vo0319yvR3rlnC2TdzMeBeUQ/n6ivPsCCL6SF8UTWT
XZJoTEfmp+Ma4zup/mEs23uO/FQ0J3LmSgICtXzPCA09M/ffj2UgTENdTHDltQxl
nQpzF+U40+bg/2PQ83XOTQJbZVbU2FnP/MitSYycxemLJXzbdsIxQhQy0VmTY73E
ZFemHVTbzEzcsCJRak4AyPZ9Zpi2uozHA8r1PqtnDzsN5FBFwuJxCuc+F8QeHh9e
QoyfsotkA6BO0LBqWNvE
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 55610A25E41364E9D8535BBE8E6AC51ACD4CEE49F887E26156B3E20C8CC078BA
    Session-ID-ctx:
    Resumption PSK: 606625EEBE3DB38271CF1EA95353EF117F951A63DC0D5806477D0785310A22892C5450EF9F49CC2F253B3C2966393F7D
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - dc 1b 67 7e 6b 49 ec f9-e1 0a 8a 6e cb ac b4 e6   ..g~kI.....n....
    0010 - e5 5a 7a f5 e6 8b 8b af-b5 cd 4f ba 81 b7 c9 fe   .Zz.......O.....
    0020 - 73 bd ad bf 31 49 87 bf-81 4b 06 7d 12 94 7e 67   s...1I...K.}..~g
    0030 - d3 8e 17 d1 fa af 33 0e-ae 56 25 05 ee b5 91 67   ......3..V%....g
    0040 - 76 70 3c f9 9e 04 e4 c4-69 42 45 dc 5f 60 bf c7   vp<.....iBE._`..
    0050 - cb 1b 2d 69 a6 d0 c4 85-42 6b e7 79 be ec 4f 1b   ..-i....Bk.y..O.
    0060 - 39 13 1e 21 7c ac 4f c1-47 f4 49 db fe 68 1a e9   9..!|.O.G.I..h..
    0070 - 3d 0e dc 8a c3 d1 54 29-36 6a 8f f7 7f 3b 82 9f   =.....T)6j...;..
    0080 - db 1d 9a 66 70 e1 1a 04-1a 61 2b 64 4e 45 1e 6b   ...fp....a+dNE.k
    0090 - e5 3a 03 a3 89 17 24 d8-5c d2 2d b2 0b c3 f4 c8   .:....$.\.-.....
    00a0 - 34 3b a8 6e d3 a0 07 cb-25 51 5f 75 23 fb 7e 66   4;.n....%Q_u#.~f
    00b0 - d9 53 8c 56 5f f9 f4 cd-84 6a d7 2f 32 65 50 9a   .S.V_....j./2eP.
    00c0 - c9 b6 f2 4b 6e e3 d8 fd-46 16 d4 8c 4a 92 cf 62   ...Kn...F...J..bread R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: B2887CFCE9BB540C24A0369F6381BA96346E7A72F06E0B3E8FB44E3EC42D7743
    Session-ID-ctx:
    Resumption PSK: 6D544B91A4F2077C7FE36F6C61EA1D6B1F590EF72D0F5BD388B277660D7C410A77E205D1A1308E852388EA61F411FB2C
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - dc 1b 67 7e 6b 49 ec f9-e1 0a 8a 6e cb ac b4 e6   ..g~kI.....n....
    0010 - 32 2f e7 25 84 52 a5 54-de 38 e8 75 1e 7b aa ac   2/.%.R.T.8.u.{..
    0020 - 78 8a e4 96 ed b1 c5 3a-87 f4 ce 80 af dc f0 7e   x......:.......~
    0030 - 49 d5 4d ed be 14 d0 0f-b5 ea a3 f3 1b 49 33 48   I.M..........I3H
    0040 - cb 02 d1 26 37 2f 66 94-92 3d 5e 5a 86 b9 99 cb   ...&7/f..=^Z....
    0050 - 97 b1 40 ef b0 cb b9 7d-25 9e fa c7 4e 04 ce 65   ..@....}%...N..e
    0060 - 28 82 22 89 39 33 af 7f-99 8f 59 96 76 e5 f3 ef   (.".93....Y.v...
    0070 - 37 f9 46 3c a7 34 ee 97-fe b5 28 6a fc a3 ed 27   7.F<.4....(j...'
    0080 - 52 b6 a0 c9 9e 9c c0 0f-04 34 6d 89 1d 31 e4 05   R........4m..1..
    0090 - 3e 86 9b a9 38 1d 98 1b-29 db 7f 32 71 8a 73 1c   >...8...)..2q.s.
    00a0 - 3c 7b 28 60 2b 12 74 86-fd 46 c6 85 5d a0 e0 eb   <{(`+.t..F..]...
    00b0 - 74 08 fb 8d b8 08 f0 c6-72 1c 6e cb 53 86 03 6b   t.......r.n.S..k
    00c0 - a4 99 71 3d 3d 8b 31 a0-f0 73 e0 92 6f 29 98 13   ..q==.1..s..o)..

read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
## Notas
el comando Openssl es usado para crear, convertir, gestionan la Certificados SSL
## Referencias 
https://geekflare.com/es/openssl-commands-certificates/