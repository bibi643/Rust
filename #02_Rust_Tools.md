# Rust command tools
Tools such as cargo and rustfmt. 
- cargo to keep track dependencies and initialize project.
cargo is for building running and creating rust project.
- rustfmt to automate formatting rust code.


# Cargo to initialize a new project 
It should have been installed by default but type cargo in the prompt to check just in case.
We have to be in the directory where we want to create the cargo project.

```rust
cargo new project_folder_project

cargo new tutorial2
```

In Vs Code we can see a folder inside we have a src folder and gitignore and a Cargo.toml(Toms Obvious Minimal Language)... All this has been created by cargo.
**src** folder is where all the codes will go.


## Run a code from a cargo project

We have to go inside the project folder, here tutorial2 (doing a cd in the terminal)
### Cargo build
We run **cargo build**.

This will create more files such as:
- Cargo.lock: This will manage all the versions
- target: contains the exec files.
  


```bash
cargo build
cd target
cd debug
./tutorial2


>>> Hello world!
```
### Cargo run


Instead all those steps we can run **cargo run** and this will automatically run the program.
```bash
~/Desktop/Rust_tuto/tutorial2$ cargo run
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/tutorial2`
>>> Hello, world!
```


### Cargo check


```bash
~/Desktop/Rust_tuto/tutorial2$ cargo check
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.00s
     Running `target/debug/tutorial2`

```

This does not return anything. This just check if the script is ready to be compiled without compiling it.

# rustfmt
Go inside the src folder where the codes are and run the comand **rustfmt file_name.rs**

It will automatically reformat the file putting the correct indentation for example.
```bash

/Desktop/Rust_tuto/tutorial2/src$ rustfmt main.rs
```

# Entry point

We want to have in src a:
- main.rs file
- main function

We need this to run a script properly. **No entry point no party**


