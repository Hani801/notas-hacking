## Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip)
## Solución
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ wget https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
--2024-02-26 13:03:16--  https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 4520 (4.4K) [application/octet-stream]
Saving to: ‘Addadshashanammu.zip’

Addadshashanammu.zip          100%[=================================================>]   4.41K  --.-KB/s    in 0s

2024-02-26 13:03:24 (20.4 MB/s) - ‘Addadshashanammu.zip’ saved [4520/4520]

hani06@DESKTOP-4NE4RTQ:~/picosCTF$ ls
Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ unzip Addadshashanammu.zip
-bash: unzip: command not found
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ sudo apt install unzip
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Suggested packages:
  zip
The following NEW packages will be installed:
  unzip
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 166 kB of archives.
After this operation, 388 kB of additional disk space will be used.
Get:1 http://deb.debian.org/debian bookworm/main amd64 unzip amd64 6.0-28 [166 kB]
Fetched 166 kB in 16s (10.1 kB/s)
Selecting previously unselected package unzip.
(Reading database ... 11637 files and directories currently installed.)
Preparing to unpack .../unzip_6.0-28_amd64.deb ...
Unpacking unzip (6.0-28) ...
Setting up unzip (6.0-28) ...
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ unzip Addadshashanammu.zip
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ ls
Addadshashanammu  Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
Addadshashanammu/     Addadshashanammu.zip
hani06@DESKTOP-4NE4RTQ:~/picosCTF$ cd Addadshashanammu
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu$ ls
Almurbalarammi
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
-bash: cd: too many arguments
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu$ tree
-bash: tree: command not found
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu$ cd Almurbalarammi/Ashalmimilkala/
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ ls
Assurnabitashpi
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet
-bash: cd: Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet: Not a directory
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala$ cd Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ cat fang-of-haynekhtnamet
 HH/lib64/ld-linux-x86-64.so.2GNUGNU "!@����a     ~= Y h "libc.so.6puts__cxa_finalize__libc_start_       HterTMCloneTable__gmon_start___ITM_registerTMCloneTableui     1
 Ht5
 %
 @%
 h%
H=HHPTLH
 DH=
 UH
 H9HtHZ
]f.]@f.H=i
 H5b
 UH)HHHH?HHtH!
 Ht]f]@f.=
H/H=    ]fDUH]fUHH=]f.DAWAVIAUATL%F UH-F SAIL)HWHt 1LLDAHH9u[]A\A]A^A_Ðf.*ZAP!* picoCTF{l3v3l_up!_t4k o`BE B(H0H8M@r8A0A(B BBB0;*3$"D\RAC
  GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.08Tt`  
  $ z  @R Yx   `e ~0+ :  "crtstuff.cderegister_tm_clones__do_global_dtors_auxcompleted.7698__do_global_dtors_aux_fini_array_entryframe_dummy__frame_dummy_init_array_entryfang-of-haynekhtnamet.c__FRAME_END____init_array_end_DYNAMIC__init_array_start__GNU_EH_FRAME_HDR_GLOBAL_OFFSET_TABLE___libc_csu_fini_ITM_deregisterTMCloneTableputs@@GLIBC_2.2.5_edata__libc_start_main@@GLIBC_2.2.5__data_start__gmon_start____dso_handle_IO_stdin_used__libc_csu_init__bss_startmain__TMC_END___ITM_registerTMCloneTable__cxa_finalize@@GLIBC_2   0)@(;hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ame.init_array.fini_array.dynamic.data.bss.comment
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ls -la
total 12
drwxr-xr-x 1 hani06 hani06 4096 Mar 15  2021 .
drwxr-xr-x 1 hani06 hani06 4096 Mar 15  2021 ..
-rwxr-xr-x 1 hani06 hani06 8320 Mar 15  2021 fang-of-haynekhtnamet
hani06@DESKTOP-4NE4RTQ:~/picosCTF/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku$ ./fang-of-haynekhtnamet
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}
## Notas

## Referencias
