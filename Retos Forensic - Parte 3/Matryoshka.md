## Objetivo
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Solución
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ binwalk dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg
651600        0x9F150         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ unzip dolls.jpg
Archive:  dolls.jpg
warning [dolls.jpg]:  272492 extra bytes at beginning or within zipfile
  (attempting to process anyway)
  inflating: base_images/2_c.jpg
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ cd ..
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic$ mkdir macrohard
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic$ cd macrohard/
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm
-bash: https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm: No such file or directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ wget https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm
--2024-03-20 13:01:13--  https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100093 (98K) [application/octet-stream]
Saving to: ‘Forensics is fun.pptm’

Forensics is fun.pptm      100%[=====================================>]  97.75K   449KB/s    in 0.2s

2024-03-20 13:01:14 (449 KB/s) - ‘Forensics is fun.pptm’ saved [100093/100093]

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ ls -la
total 100
drwxrwxrwx 1 hani06 hani06   4096 Mar 20 13:01  .
drwxrwxrwx 1 hani06 hani06   4096 Mar 20 13:00  ..
-rwxrwxrwx 1 hani06 hani06 100093 Mar 23  2021 'Forensics is fun.pptm'
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ cat hidden | tr -d ' ' | base64 -d
cat: hidden: No such file or directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ ls Forensics\ is\ fun.pptm
'Forensics is fun.pptm'
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ cat hidden | tr -d ' ' | base64 -d
cat: hidden: No such file or directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ cd Forensics\ is\ fun.pptm
-bash: cd: Forensics is fun.pptm: Not a directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/macrohard$ cd ..
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic$ cd Matryoshkadoll/
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ bimwalk dolls.jpg
-bash: bimwalk: command not found
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ binwalk dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg
651600        0x9F150         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ bin
bind            bindfltapi.dll  binwalk
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg
651600        0x9F150         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ ls
base_images  dolls.jpg  _dolls.jpg.extracted
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll$ cd _dolls.jpg.extracted/
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted$ ls
4286C.zip  base_images
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted$ cd base_images/
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ ls
2_c.jpg
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ cd 2_c.jpg
-bash: cd: 2_c.jpg: Not a directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ binwalk 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ la
-bash: la: command not found
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ ls
2_c.jpg  _2_c.jpg.extracted
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ ls
2_c.jpg  _2_c.jpg.extracted
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ cd _2
-bash: cd: _2: No such file or directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ ls
2DD3B.zip  base_images
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted$ cd ..
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/base_images
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79806, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79806, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ ls
3_c.jpg  _3_c.jpg.extracted
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/bases_images
-bash: cd: _3_c.jpg.extracted/bases_images: No such file or directory
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/base_images
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 62, uncompressed size: 81, name: flag.txt
79784         0x137A8         End of Zip archive, footer length: 22

hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls
136DA.zip  flag.txt
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/Matryoshkadoll/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}


## Notas
