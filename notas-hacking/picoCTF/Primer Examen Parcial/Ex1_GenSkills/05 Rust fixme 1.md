#### Description

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag! Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).

**Solución** 

picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}

**Notas adicionales** 

```

fergll@FerGLl:/mnt/c/Users/ferch/Documents$ wget https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ tar -xzvf fixme1.tar.gz
fixme1/
fixme1/Cargo.toml
fixme1/Cargo.lock
fixme1/src/
fixme1/src/main.rs
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cd fixme1
fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme1$ cat src/main.rs
use xor_cryptor::XORCryptor;

fn main() {
    // Key for decryption
    let key = String::from("CSUCKS") // How do we end statements in Rust?

    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", "7f", "5a", "60", "50", "11", "38", "1f", "3a", "60", "e9", "62", "20", "0c", "e6", "50", "d3", "35"];

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        ret; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    println!(
        ":?", // How do we print out a variable in the println function?
        String::from_utf8_lossy(&decrypted_buffer)
    );

fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme1$ sudo apt update && sudo apt install cargo -y

fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme1$ nano src/main.rs

codigo del nano:
use xor_cryptor::XORCryptor;

fn main() {
    // Key for decryption
    let key = String::from("CSUCKS"); // How do we end statements in Rust?

    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", ">

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    println!(
        "{}", // How do we print out a variable in the println function?
        String::from_utf8_lossy(&decrypted_buffer)
        );
}

fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme1$ cargo run
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/mnt/c/Users/ferch/Documents/fixme1)
    Finished dev [unoptimized + debuginfo] target(s) in 6.97s
     Running `target/debug/rust_proj`
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}

```

- - **Depuración de sintaxis (Debugging):** Editamos el archivo `src/main.rs` con `nano` para corregir tres errores de sintaxis comunes en Rust:
    
    - **Punto y coma:** Agregamos `;` al final de la declaración de la variable `key`.
        
    - **Palabra reservada:** Corregimos el error de dedo en la instrucción `return`.
        
    - **Formato de impresión:** Cambiamos el placeholder incorrecto por `{}` dentro de la macro `println!` para poder visualizar el string de la bandera.
        
- **Compilación y ejecución:** Ejecutamos el comando `cargo run`, el cual descargó automáticamente la dependencia de criptografía (`xor_cryptor`), compiló el código corregido y ejecutó el programa.
    
- **Obtención de la Flag:** El programa procesó los valores hexadecimales con la llave proporcionada y mostró la bandera **picoCTF{...}** directamente en la terminal.

**Referencias**
