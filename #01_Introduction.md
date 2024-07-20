# Installation

For Linux and Mac just run
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```


# Writing in rust
 create a file main.rs to create a rust file.

 ```rust
fn main() {
    println!("hello world"!)
}
```
println!. the ! means we are running a macro

# Run a script
From command prompt, go the the folder where the file is and run
```rust
rustc file_name.rs
```

This will create a **executable file**. Note that if an executable is created on linux, it will only run on linux and mac.
To run this file just type ./file_name on linux and mac, being obviously in the folder where the file is.



