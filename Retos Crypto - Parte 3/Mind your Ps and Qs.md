## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
## Solución
>>> p = 2434792384523484381583634042478415057961
>>> q = 650809615742055581459820253356987396346063
>>> m = p * q
>>> m
1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> e = 65537
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> tn = p(p-1) * (q-1)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'int' object is not callable
>>> tn = (p-1) * (q-1)
>>> d = pow(e, -1, tn)
>>> m= pow(c,d,n)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'n' is not defined. Did you mean: 'tn'?
>>> n = p * q
>>> n
1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> m= pow(c,d,n)
>>> bytes.fromhex( hex(m)[2:] )
b'picoCTF{sma11_N_n0_g0od_73918962}'
## Notas
