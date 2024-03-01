## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Solución
haniara-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
--2024-02-29 01:29:57--  https://jupiter.challenges.picoctf.org/static/495d43ee4a2b9f345a4307d053b4d88d/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file.1'

file.1              100%[==================>]  14.21K  --.-KB/s    in 0s      

2024-02-29 01:29:57 (401 MB/s) - 'file.1' saved [14551/14551]

haniara-picoctf@webshell:~$ file warm 
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=506b7be935d8940c672ab0d40d2e03ebd746155b, with debug_info, not stripped
haniara-picoctf@webshell:~$ ls -la
total 128
drwxr-xr-x 3 haniara-picoctf haniara-picoctf  4096 Feb 29 01:29 .
drwxr-xr-x 3 root            root               29 Feb 26 18:18 ..
-rw------- 1 haniara-picoctf haniara-picoctf   538 Feb 28 19:23 .bash_history
-rw-r--r-- 1 haniara-picoctf haniara-picoctf   220 Feb 26 18:18 .bash_logout
-rw-r--r-- 1 haniara-picoctf haniara-picoctf  3771 Feb 26 18:18 .bashrc
drwxrwxr-x 3 haniara-picoctf haniara-picoctf    19 Feb 28 19:08 .local
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf     0 Feb 26 18:56 .ltdis.x86_64.txt
-rw-r--r-- 1 haniara-picoctf haniara-picoctf   807 Feb 26 18:18 .profile
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf   167 Feb 29 01:29 .wget-hsts
-rw-r--r-- 1 root            root             4443 Feb 29 01:29 README.txt
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf  1278 Mar 16  2023 code.py
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf    27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf  1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf 14551 Oct 26  2020 file
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf 14551 Oct 26  2020 file.1
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf    34 Mar 16  2021 flag
-rwxrwxrwx 1 haniara-picoctf haniara-picoctf   785 Mar 16  2021 ltdis.sh
-rw------- 1 haniara-picoctf haniara-picoctf  2089 Feb 28 19:09 nano.231.save
-rw------- 1 haniara-picoctf haniara-picoctf  2089 Feb 28 19:10 nano.235.save
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf  1668 Feb 26 18:56 static.ltdis.strings.txt
-rw-rw-r-- 1 haniara-picoctf haniara-picoctf  6497 Feb 26 18:56 static.ltdis.x86_64.txt
-rwxrwxr-x 1 haniara-picoctf haniara-picoctf 10936 Mar 16  2021 warm
haniara-picoctf@webshell:~$ /.warm
-bash: /.warm: No such file or directory
haniara-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
haniara-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
haniara-picoctf@webshell:~$ ls
README.txt    file      nano.231.save             static.ltdis.x86_64.txt
code.py       file.1    nano.235.save             warm
codebook.txt  flag      static
convertme.py  ltdis.sh  static.ltdis.strings.txt
haniara-picoctf@webshell:~$ cat file | grep pico
picoCTF{grep_is_good_to_find_things_dba08a45}

## Referencias
