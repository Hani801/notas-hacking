## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de acceso al nivel
Usuario: bandit16@bandit.labs.overthewire.org
Contraseña: JQttfApK4SeyHwDlI9SXGR50qclOAil1
Puerto: 2220
## Solución
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 20 17:51:06 2024 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 20 17:50:06 2024 GMT; NotAfter: Feb 20 17:51:06 2024 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEQ9wEgDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjQwMjIwMTc1MDA2WhcNMjQwMjIwMTc1MTA2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDA
gdd50zQdwKnADuCYAoUSFvGreD2Mr/e6QZK+31XsKXCd/+cGHdmkqerggVlwno8T
3lmAaRw+Pk/nNdn3xJEGGq5guV2YhAnT+IQgP6+76ii/4gUCQxnaTtmslJDSfv7i
km+qYsFRL1YdtOo5od2etkLdorXGqGcIrB6ilCgKgQ2Q7FqMjh7n37HPk8yaWCwX
M/JZ7jkXw4mf2Un9UILgo/oJfR0JhMq6cDkHztG0E6j5ruknDeeOMGimH9pmzaa9
xdJe1GTtk+v03FIng0IfHi0HVPUCN8dl9rKLzn/LKZ3UftyffIErE7nDCLaGpVBK
DQzkq5gMPShGa1RT7nkFAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBh
XmVUELbEPhoHaMrhwHyd24bRzYiiOemi75OA6QywOLh7moC8MGKvtI0mHhhA+lfB
eEvOOPwL5om4culG+KnC24fdWzwX/PPtkYKocNSrIQINrVhTwBbGwnC+WCSYizZS
43Zav+szrJ6H66qO4x4wXU9p1qC24dIpY5dfBsy4m8P/XzUtg68YJng1EIuGM6DF
CnMWXUB0cfUgBsbWPMrQlJd5sHifKeglK3kBCXn3zb9T881YbLNAwMK2a5SnPdh8
eTg1e7pdNYwPvHcxYPySGyQCkLpLHduWUxVNrUfsVHrxI6rrHynZ5vv4+ulAmhAc
YoU33/wx/D1oycw1GLHh
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
    Session-ID: 3B4D0C05545E352619D24B2B1B4B9B7139E44A95DCE637E9061F6484818077E6
    Session-ID-ctx:
    Resumption PSK: 2E43966034EEEB18A66CA2A4C1D78C8D3C2CB0E60DEF265CA53A507378A9746C73E08E23174BAB26CCC12529B0FB63E2
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 92 ed 0d d5 75 f9 0c 95-ed 08 73 73 af f3 6c c3   ....u.....ss..l.
    0010 - 08 c6 2f 56 33 5a 7e 12-24 57 a1 56 9e 97 f0 68   ../V3Z~.$W.V...h
    0020 - 5e cd d2 22 b5 ec 40 69-d4 d1 a1 df 6f ac 9f fc   ^.."..@i....o...
    0030 - 6f 2f 46 62 fb f6 75 a0-e8 20 e6 25 e6 65 73 02   o/Fb..u.. .%.es.
    0040 - c9 3b 1e 83 58 00 ad fd-36 a8 7f 21 c9 f8 a3 69   .;..X...6..!...i
    0050 - 30 b2 99 d9 57 c3 30 88-04 b9 7c e2 9b 56 f7 33   0...W.0...|..V.3
    0060 - 1e b0 45 e7 1f cb f7 f5-31 18 92 0c fe 0c a8 55   ..E.....1......U
    0070 - d8 a5 19 7a 10 32 4e aa-32 e0 4f 70 1f 91 05 2c   ...z.2N.2.Op...,
    0080 - 7d 56 c8 65 45 97 aa c6-54 92 99 3f 2b 90 a9 26   }V.eE...T..?+..&
    0090 - 1e 1d c0 76 5a 0b ce 5c-df 6e e6 e0 86 95 4d 81   ...vZ..\.n....M.
    00a0 - 76 d2 00 ef f1 cc d4 41-a3 16 24 b5 db 4d 8a dd   v......A..$..M..
    00b0 - b6 db c2 80 ac d5 ba dd-06 05 2a 1c 21 0d be 6b   ..........*.!..k
    00c0 - ed b1 9a f6 6e 36 74 f2-a2 df 89 6e 28 74 6f 4a   ....n6t....n(toJ

    Start Time: 1708540002
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 54CA73A8814D0B7FD1FB5CE158A3366501BEA594A980B4BB135583C5283F2C90
    Session-ID-ctx:
    Resumption PSK: 248F314C18B1F7FF5CD62A8D0411E96B0B474BCD4592BEF35CF87FAA37D11F6A937680436614DEF02AE8B7E90598F4B4
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 92 ed 0d d5 75 f9 0c 95-ed 08 73 73 af f3 6c c3   ....u.....ss..l.
    0010 - 4e 91 29 5f 7d 85 0d 5e-ca 01 80 7d 2a c0 bb 2f   N.)_}..^...}*../
    0020 - 83 fe 16 f8 7e 09 d3 4d-ca 02 bf 47 fc 2a e3 7e   ....~..M...G.*.~
    0030 - 1a 95 42 21 81 24 54 7a-be 84 19 04 45 25 44 50   ..B!.$Tz....E%DP
    0040 - d4 e2 16 2b db 82 01 26-47 f4 ab f6 90 10 3b b8   ...+...&G.....;.
    0050 - 2f 3f 76 1b 0e 22 e7 56-a4 1b 66 89 ff c1 c3 3e   /?v..".V..f....>
    0060 - 2f 76 cc 96 0c 61 da 75-a1 58 02 1a 44 cf ac e0   /v...a.u.X..D...
    0070 - 01 f4 17 44 1f 6a 37 19-1b 96 84 18 d4 7b 48 70   ...D.j7......{Hp
    0080 - 9e 56 0d b6 c4 29 7a b4-a1 d2 7e 88 c9 b7 5b a3   .V...)z...~...[.
    0090 - 7c 4b 31 f7 38 67 af a4-b0 ab 8a c9 ca 41 d7 2e   |K1.8g.......A..
    00a0 - 1d 6b f0 4c 71 60 72 d9-2f ec 17 6f a8 6f e7 af   .k.Lq`r./..o.o..
    00b0 - a2 b2 b8 87 37 0a b3 b4-37 3d e8 fc 01 8f e9 89   ....7...7=......
    00c0 - ec d2 62 d3 b4 36 e7 46-a3 35 62 69 3d ff b0 51   ..b..6.F.5bi=..Q

    Start Time: 1708540002
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$ exit
logout
Connection to bandit.labs.overthewire.org closed.

C:\Users\Hani>cd Desktop

C:\Users\Hani\Desktop>dir
 El volumen de la unidad C no tiene etiqueta.
 El número de serie del volumen es: 2E1F-C92B

 Directorio de C:\Users\Hani\Desktop

21/02/2024  12:28 p. m.    <DIR>          .
21/02/2024  12:28 p. m.    <DIR>          ..
21/02/2024  12:28 p. m.             1,700 lallave.txt
21/02/2024  11:23 a. m.             1,052 ZinjaI.lnk
               2 archivos          2,752 bytes
               2 dirs  142,751,694,848 bytes libres

C:\Users\Hani\Desktop>ssh bandit17@bandit.labs.overthewire.org -p 2220 -i lallave.txt
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames


      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit17@bandit:~$ cat /etc/ba
bandit_pass/       bash.bashrc        bash_completion    bash_completion.d/
bandit17@bandit:~$ cat /etc/ba
bandit_pass/       bash.bashrc        bash_completion    bash_completion.d/
bandit17@bandit:~$ cat /etc/bandit_pass/bandit
bandit0   bandit11  bandit14  bandit17  bandit2   bandit22  bandit25  bandit28  bandit30  bandit33  bandit6   bandit9
bandit1   bandit12  bandit15  bandit18  bandit20  bandit23  bandit26  bandit29  bandit31  bandit4   bandit7
bandit10  bandit13  bandit16  bandit19  bandit21  bandit24  bandit27  bandit3   bandit32  bandit5   bandit8
bandit17@bandit:~$ cat /etc/bandit_pass/bandit
bandit0   bandit11  bandit14  bandit17  bandit2   bandit22  bandit25  bandit28  bandit30  bandit33  bandit6   bandit9
bandit1   bandit12  bandit15  bandit18  bandit20  bandit23  bandit26  bandit29  bandit31  bandit4   bandit7
bandit10  bandit13  bandit16  bandit19  bandit21  bandit24  bandit27  bandit3   bandit32  bandit5   bandit8
bandit17@bandit:~$ cat /etc/bandit_pass/bandit
bandit0   bandit11  bandit14  bandit17  bandit2   bandit22  bandit25  bandit28  bandit30  bandit33  bandit6   bandit9
bandit1   bandit12  bandit15  bandit18  bandit20  bandit23  bandit26  bandit29  bandit31  bandit4   bandit7
bandit10  bandit13  bandit16  bandit19  bandit21  bandit24  bandit27  bandit3   bandit32  bandit5   bandit8
bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e

## Notas
## Referencias