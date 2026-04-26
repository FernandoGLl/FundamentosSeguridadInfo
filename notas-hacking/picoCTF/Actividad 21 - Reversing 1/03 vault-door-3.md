#### Description

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://challenge-files.picoctf.net/c_fickle_tempest/4cff24ee8b551078be8c14758fae20ab4a2dca78746aef367bc854491b8ee465/VaultDoor3.java)

**Solución**

**`picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_e60bc2}`**

**Notas adicionales**

En la terminal de java script de firefox se realizo lo siguiente para poder obtener la bandera de manera ordenada.

```
var password = "jU5t_a_sna_3lpm1cg04e_u_4_m6rb42";  

undefined  

var buffer = Array(32);  

undefined  

for (i=0; i<8; i++) { buffer[i] = password.charAt(i); } for (; i<16; i++) { buffer[i] = password.charAt(23-i);…  

"g"  

console.log(buffer.join(""))  

jU5t_a_s1mpl3_an4gr4m_4_u_e60bc2

```

luego de esto se verifico ejecutnado el programa original:
```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cat VaultDoor3.java
import java.util.*;

class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
        String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
        if (vaultDoor.checkPassword(input)) {
            System.out.println("Access granted.");
        } else {
            System.out.println("Access denied!");
        }
    }

    // Our security monitoring team has noticed some intrusions on some of the
    // less secure doors. Dr. Evil has asked me specifically to build a stronger
    // vault door to protect his Doomsday plans. I just *know* this door will
    // keep all of those nosy agents out of our business. Mwa ha!
    //
    // -Minion #2671
    public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
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
        return s.equals("jU5t_a_sna_3lpm1cg04e_u_4_m6rb42");
    }
}fergll@FerGLl:/mnt/c/Users/ferch/Documents$ javac VaultDoor3.java
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ java VaultDoor3
Enter vault password: picoCTF(jU5t_a_s1mpl3_an4gr4m_4_u_e60bc2)
Access granted.

```

**Referencias** 

