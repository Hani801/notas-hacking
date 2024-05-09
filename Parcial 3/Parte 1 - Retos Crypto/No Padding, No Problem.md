## Objetivo
Oracles can be your best friend, they will decrypt anything, except the flag's ciphertext. How will you break it? Connect with `nc mercury.picoctf.net 28517`.
## Solución
C:\Users\Hani\Documents\picoCTF>python message.py
[x] Opening connection to mercury.picoctf.net on port 28517
[x] Opening connection to mercury.picoctf.net on port 28517: Trying 18.189.209.142
[+] Opening connection to mercury.picoctf.net on port 28517: Done
b'Welcome to the Padding Oracle Challenge\nThis oracle will take anything you give it and decrypt using RSA. It will not accept the ciphertext with the secret message... Good Luck!\n\n\nn:'
82079404398051393295804829202676381065384360115398174701208873889593750786490237942374274650224295834112391976545111600108733287925412079562419098531686488262348432714409536141162940417555437101104453068208314363183083547457516460603744212594048335884799177687248716813013579411725871122217326827901665721169
b'e:'
65537
b'ciphertext:'
72304758945422293905972053721674097496822734398043293896276810260555285534892511866676671735766711513032206112405905185896977744705646274255363770313317446169684408836367866861021232769504697579248436614641663638605130736550125972870479959343362428366309649636655368137445254515864566270527367520299289799488
b'\n\nGive me ciphertext to decrypt:'
b' Here you go:'
580550060391700078946913236734911770139931497702556153513487440893406629034802718534645538074938502890769281669222390720762
b'picoCTF{m4yb3_Th0se_m3s54g3s_4r3_difurrent_4005534}'
[*] Closed connection to mercury.picoctf.net port 28517
## Notas