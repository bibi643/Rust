# Arithmetic

**Overflow** is when for example we assigned a variable to 300 when the type is u8.
**//** is the way to comment in Rust.
```rust
fn main() {
    let x: u8 =9; // 0-255
    let y: i8= 10; //-128 to 127

    println!("Hello, world!");
}

```
## General operations Warnings

### Type error
This would return an error because x and y are not the same type!!!

```rust
fn main() {
    let x: u8 =9; // 0-255
    let y: i8= 10; //-128 to 127

    let z = x + y

    println!("{}",z);
}
```

This would return an error too, because the result goes from u8 to the next level.
The result is not an u8 anymore, so we dont't have enough bytes to display the result.
```rust
fn main() {
    let x: u8 =255; // 0-255
    let y: u8= 10; // 0-255

    let z = x + y

    println!("{}",z);
}
```

Same here. The result will be a negative number which is not a u8 type.

```rust
fn main() {
    let x: u8 =1; // 0-255
    let y: u8= 10; // 0-255

    let z = x - y

    println!("{}",z);
}
```


## Arithmetic operations


```rust
fn main() {
    let x: u8 =255; // 0-255
    let y: i8= 10; //-128 to 127

    let z = x / y;
    println!("{}",z);
}

>>>25
```

This works. Because the results is always the same type as the types of the operand.

To actually obtain a float we need to change the datatype of the operants.
```rust
fn main() {
    let x: f64 =255.0; // 0-255
    let y: f64= 10.0; //-128 to 127

    let z = x / y;
    println!("{}",z);
}
```


# Type casting 
- option 1: writing the type directly after the value
```rust
fn main() {
    let x =255.0f32;
    let y= 10.0f32; 

    let z = x / y;
    println!("{}",z);
```

- option 2: using underscore after the value

```rust
fn main() {
    let x =255.0_f32;
    let y= 10.0_f32; 

    let z = x / y;
    println!("{}",z);
```

- option3: using as keyword

```rust
fn main() {
    let x =255.0 as f64;
    let y= 10.0 as f32; 

    let z = x / (y as f64);
    println!("{}",z);
```
- Bonus: To make big numbers more readable, we can write 127000 like **127_000**


# Type conversion str -> number

use std::io;

```rust
fn main() {
    let mut input = String::new();
    io::stdin().read_line(&mut input).expect("Expected to read line");
    let int_input: i64 = input.trim().parse().unwrap();
    println!("{}",int_input + 2);
}
```


