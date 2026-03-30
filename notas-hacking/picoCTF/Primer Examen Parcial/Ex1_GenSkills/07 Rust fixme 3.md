#### Description

Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag! Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/dcdaf491b35c1d0f5075e9583edbbb7aaea1dffb6ad32bc000e4d87b5200ff7b/fixme3.tar.gz).

**Solución**

picoCTF{n0w_y0uv3_f1x3d_1h3m_411}

**Notas adicionales** 

```
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ tar -xzvf fixme3.tar.gz
fixme3/
fixme3/Cargo.toml
fixme3/Cargo.lock
fixme3/src/
fixme3/src/main.rs
fergll@FerGLl:/mnt/c/Users/ferch/Documents$ cd fixme3/
fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme3$ nano src/main.rs
fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme3$ cargo run
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/mnt/c/Users/ferch/Documents/fixme3)
    Finished dev [unoptimized + debuginfo] target(s) in 11.31s
     Running `target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{n0w_y0uv3_f1x3d_1h3m_411}
fergll@FerGLl:/mnt/c/Users/ferch/Documents/fixme3$


NANO:

use xor_cryptor::XORCryptor;

fn decrypt(encrypted_buffer: Vec<u8>, borrowed_string: &mut String) {
    // Key for decryption
    let key = String::from("CSUCKS");

    // Editing our borrowed value
    borrowed_string.push_str("PARTY FOUL! Here is your flag: ");

    // Create decryption object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return;
    }
    let xrc = res.unwrap();

    // Did you know you have to do "unsafe operations in Rust?
    // https://doc.rust-lang.org/book/ch19-01-unsafe-rust.html
    // Even though we have these memory safe languages, sometimes we need to do things outside of the rules
    // This is where unsafe rust comes in, something that is important to know about in order to keep things in perspec>

     unsafe {
        // Decrypt the flag operations
        let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);

        // Creating a pointer
        let decrypted_ptr = decrypted_buffer.as_ptr();
        let decrypted_len = decrypted_buffer.len();

        // Unsafe operation: calling an unsafe function that dereferences a raw pointer
        let decrypted_slice = std::slice::from_raw_parts(decrypted_ptr, decrypted_len);

        borrowed_string.push_str(&String::from_utf8_lossy(decrypted_slice));
    }
    println!("{}", borrowed_string);
}

fn main() {
    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "12", "90", "7e", "53", "63", "e1", "01", "35", ">

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();
        
    let mut party_foul = String::from("Using memory unsafe languages is a: ");
    decrypt(encrypted_buffer, &mut party_foul);


```

- **Mutabilidad:** Cambiar la variable a `let mut` y el parámetro de la función a `&mut String` para permitir la edición del texto.
    
- **Habilitar `unsafe`:** Quitar los comentarios `//` de las líneas `unsafe {` y `}` para permitir el uso de punteros.
    
- **Integridad de Datos:** Mantener los `hex_values` originales del archivo (sin recortarlos) para que el descifrado sea correcto.
    
- **Finalización:** Ejecutar `cargo run` para compilar y visualizar la bandera limpia.
**Referencias**


