Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag! Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
Hints:
- Cargo is Rust's package manager and will make your life easier. See the getting started page [here](https://doc.rust-lang.org/book/ch01-03-hello-cargo.html)
- [println!](https://doc.rust-lang.org/std/macro.println.html)
- Rust has some pretty great compiler error messages. Read them maybe?
# Solucion
Usando la terminal de linux, descargamos rust usando el comando curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh, despues creamos un nuevo projecto usando cargo new rust_fixme1, tambien usamos `cargo add xor_cryptor` para añadir el xor cryptor al proyecto despues entramos a la carpeta src del proyecto y editamos el main.rs pegando el codigo del archivo de la descripcion, nomas que lo editamos para corregir sus errores, tales como el print, el return y el ;. Finalmente desde la carpeta src usamos el comando cargo run para ejecutar el proyecto y al finalizar hasta abajo aparece la bandera.
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}