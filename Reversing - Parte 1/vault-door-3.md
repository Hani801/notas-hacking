## Objetivo
This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/a648ca6dd275b9454c5d0de6d0f6efd3/VaultDoor3.java)
## Solución
 public boolean checkPassword(String pass) {
       /* if (password.length() != 32) {
            return false;
        }*/
        String password = new String ("jU5t_a_sna_3lpm18gb41_u_4_mfr340");
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        System.out.println(s);
        return s.equals("jU5t_a_sna_3lpm18gb41_u_4_mfr340");
    }
}
hani06@DESKTOP-4NE4RTQ:/mnt/c/Users/Hani/Documents/picoCTF/reversing$ java VaultDoor3.java
Enter vault password: jU5t_a_sna_3lpm18gb41_u_4_mfr340
jU5t_a_s1mpl3_an4gr4m_4_u_1fb380
Access denied!
Bandera: picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_1fb380}
## Notas
