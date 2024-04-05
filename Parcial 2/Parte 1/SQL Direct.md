## Objetivo
Connect to this PostgreSQL server and find the flag!
Additional details will be available after launching your challenge instance.
## Solución
hani06@DESKTOP-4NE4RTQ:~$ psql -h saturn.picoctf.net -p 49545 -U postgres pico
Password for user postgres:
psql (15.6 (Debian 15.6-0+deb12u1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=#  \d
         List of relations
 Schema | Name  | Type  |  Owner
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# select * from flags;
 id | firstname | lastname  |                address
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
## Notas

## Referencias