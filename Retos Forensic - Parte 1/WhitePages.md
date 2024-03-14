## Objetivo
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://jupiter.challenges.picoctf.org/static/74274b96fe966126a1953c80762af80d/whitepages.txt) is all blank!

## Solución
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ ascii
Usage: ascii [-adxohv] [-t] [char-alias...]
   -t = one-line output  -a = vertical format
   -d = Decimal table  -o = octal table  -x = hex table  -b binary table
   -h = This help screen -v = version information
Prints all aliases of an ASCII character. Args may be chars, C \-escapes,
English names, ^-escapes, ASCII mnemonics, or numerics in decimal/octal/hex.

Dec Hex    Dec Hex    Dec Hex  Dec Hex  Dec Hex  Dec Hex   Dec Hex   Dec Hex
  0 00 NUL  16 10 DLE  32 20    48 30 0  64 40 @  80 50 P   96 60 `  112 70 p
  1 01 SOH  17 11 DC1  33 21 !  49 31 1  65 41 A  81 51 Q   97 61 a  113 71 q
  2 02 STX  18 12 DC2  34 22 "  50 32 2  66 42 B  82 52 R   98 62 b  114 72 r
  3 03 ETX  19 13 DC3  35 23 #  51 33 3  67 43 C  83 53 S   99 63 c  115 73 s
  4 04 EOT  20 14 DC4  36 24 $  52 34 4  68 44 D  84 54 T  100 64 d  116 74 t
  5 05 ENQ  21 15 NAK  37 25 %  53 35 5  69 45 E  85 55 U  101 65 e  117 75 u
  6 06 ACK  22 16 SYN  38 26 &  54 36 6  70 46 F  86 56 V  102 66 f  118 76 v
  7 07 BEL  23 17 ETB  39 27 '  55 37 7  71 47 G  87 57 W  103 67 g  119 77 w
  8 08 BS   24 18 CAN  40 28 (  56 38 8  72 48 H  88 58 X  104 68 h  120 78 x
  9 09 HT   25 19 EM   41 29 )  57 39 9  73 49 I  89 59 Y  105 69 i  121 79 y
 10 0A LF   26 1A SUB  42 2A *  58 3A :  74 4A J  90 5A Z  106 6A j  122 7A z
 11 0B VT   27 1B ESC  43 2B +  59 3B ;  75 4B K  91 5B [  107 6B k  123 7B {
 12 0C FF   28 1C FS   44 2C ,  60 3C <  76 4C L  92 5C \  108 6C l  124 7C |
 13 0D CR   29 1D GS   45 2D -  61 3D =  77 4D M  93 5D ]  109 6D m  125 7D }
 14 0E SO   30 1E RS   46 2E .  62 3E >  78 4E N  94 5E ^  110 6E n  126 7E ~
 15 0F SI   31 1F US   47 2F /  63 3F ?  79 4F O  95 5F _  111 6F o  127 7F DEL
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ xxd -l 100 -g 1 whitepages.txt
00000000: e2 80 83 e2 80 83 e2 80 83 e2 80 83 20 e2 80 83  ............ ...
00000010: 20 e2 80 83 e2 80 83 e2 80 83 e2 80 83 e2 80 83   ...............
00000020: 20 e2 80 83 e2 80 83 20 e2 80 83 e2 80 83 e2 80   ...... ........
00000030: 83 e2 80 83 20 e2 80 83 e2 80 83 20 e2 80 83 20  .... ...... ...
00000040: 20 20 e2 80 83 e2 80 83 e2 80 83 e2 80 83 e2 80    ..............
00000050: 83 20 20 e2 80 83 20 e2 80 83 e2 80 83 20 e2 80  .  ... ...... ..
00000060: 83 20 20 e2                                      .  .
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ cat whitepages.txt
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ ls
whitepages.txt
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ sudo apt install sed
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
sed is already the newest version (4.9-1).
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ sed 's/\xe2\x80\x83/0/g'whitepages.txt
^C
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ sed 's/\xe2\x80\x83/0/g' whitepages.txt
0000 0 00000 00 0000 00 0   00000  0 00 0  000  0  0    0 0000  0 0 0 000 000  00000 0 00000 0 00000 00 0000 00 0 0 00  0 000 0 0 000 0 00 000000 0 00000 0 0 0 0 0000 00 00  000 00 00 0 0000  00 000000 0 00 00 000 0 0 0000  0 00    0 0 00 00 000 000 0 00  00 0000000 00  000 000000 0000 00 00000 0 0000  0 00 0  0 000   0 0 00 00 00    0 0 0 0 0 00   00 000 0000 000000 0 00 00 000 0 0 0 00000 00    0 0 00 00 0 0 000000 0 00000 00 0000 00 00  0 0 00  000000  000000  000000 000000 000  00  0    0   00 00  000 00  00 0 0   00  00 000000 00000 0   0  00  00 0 00 0  0000 000000 0 00000  0 00 0   0 000   0 000   00  0  000 00   0 0 0   00 00  00   0  0 00000 0  0000 000000 0 00000 00000 00 0000000  000 00  0 0 00  00 000  000 00  00  0000 0 00000 00 0000 00 0   00000  0 00 0  000  0  0    0 0000  0 0 0 000 000  00    0  0  0   00  0    0   0 000 0     0  0000 0  0  000  0  000 0     0   00  0   00000  0000 0  000  0  00 0 0   00  0 0     0  0000 0   00 00  00 0 0 0     0  000  0   00 00  00 0 0  0000 0   0 000  00 0 0  00 000 0     0  00 0 0   000 0   0 0 0  0000 0  0  000 0     0  000  00  0 0 00  0 000  00  000  00 000  0   0  000  0  00 0000  000000  0 0 0  000  00  00 000  000 00   00000   00 0  00  000   00000  000 00  0 0000  0   0  000  0  000  00  0  00  00  000  0 0 0  00 000  00 0 0  000 000  00 00  00 0 00  0 0 00  0  00     0 0000 0 00000 00 0000 00 hani06@DESKTOP-4NE4RTQ:/mnt/c/Usershani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/forensic/whitpages$ sed 's/\xe2\x80\x83/0/g' whitepages.txt | sed 's/\x20/1/g'
00001010000010010000100101110000011010010110001101101111010000110101010001000110000010100000101000001001000010010101001101000101010001010010000001010000010101010100001001001100010010010100001100100000010100100100010101000011010011110101001001000100010100110010000000100110001000000100001001000001010000110100101101000111010100100100111101010101010011100100010000100000010100100100010101010000010011110101001001010100000010100000100100001001001101010011000000110000001100000010000001000110011011110111001001100010011001010111001100100000010000010111011001100101001011000010000001010000011010010111010001110100011100110110001001110101011100100110011101101000001011000010000001010000010000010010000000110001001101010011001000110001001100110000101000001001000010010111000001101001011000110110111101000011010101000100011001111011011011100110111101110100010111110110000101101100011011000101111101110011011100000110000101100011011001010111001101011111011000010111001001100101010111110110001101110010011001010110000101110100011001010110010001011111011001010111000101110101011000010110110001011111011000110011010100110100011001100011001000110111011000110110010000110000001101010110001100110010001100010011100000111001011001100011100000110001001101000011011101100011011000110011011001100110001101010110010001100101011000100011001001100101001101010011011001111101000010100000100100001001


## Notas
