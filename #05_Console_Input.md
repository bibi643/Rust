# Console Input

## Vocabulary

### Prelude
_Definition_:
 
Prelude is a list of things that Rust **automatically imports into every Rust program**. It kept as small as possible and is focused on things, particularly traits, which are used in almost every single Rust program.



### Crates
Package or library

### Module

Piece of functionalities inside creates


## Import a module

Console input is not in the prelude so we have to manually import it.

_use std::io;

**::** is path separator operator. To pass from a library to a module or a module to a function.

This means we are using the **std library and bring in the io module**


# Console input usecase

1- We need to declare a variable to store the user input.
2- Collect the input

_io::stdin()_ is to grab the stdin() from the io module.

_.expect("Failed to read line") is kind of error handling. If the script cannot read the line it will raise an error printing the message inside expect().


```rust
use std::io;





fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).expect("failed to read line");
    println!("{}",input);
}
```



