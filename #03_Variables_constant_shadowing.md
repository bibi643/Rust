# Variables, Constants and Shadowing.

## Variables

Mutablity: Mutability I think is about values. This does not apply to data type. If I make a variable mutuable, this means I can change the value. 4 ->5.
I cannot change the type. 

## Method 1 (let)
 let var_name: data_type = var_value

```rust
fn main() {
    let x = 4;
    println!("x is {}", x);
}
```
In vs code it is automatically choosing the corresponding type, probably because I download an extension that do this.

The in the terminal, being in the correct folder, run *cargo run*.

- Example of what we think we can do but wew cannot in static typed language.


```rust
fn main() {
    let x = 4;

    println!("x is {}", x);

    x = 5;
    
    println!("x is {}", x);
}

>>>error[E0384]: cannot assign twice to immutable variable `x`
```

By default, **variables are immutable**. So that is why we cannot not change x without re defining it. 

There 2 ways to solve this "problem".

- Option 1: make the variable mutuable (**mut**)

Now I am allowed to change x along the script.



```rust
fn main() {
    let mut x = 4;

    println!("x is {}", x);

    let x = 5;
    
    println!("x is {}", x);
}

>>>x is 4
x is 5
```

- Option 2: Overwriting the variable using let.

This overwrite but the variable is still immutable.

```rust
fn main() {
    let x = 4;

    println!("x is {}", x);

    let x = 5;
    
    println!("x is {}", x);
}

>>>x is 4
x is 5
```
The second works because wwe use **let** twice!!!
Note that this option allows us to change the type of the variable.

```rust
fn main() {
    let x = 4;

    println!("x is {}", x);

    let x = "Hello";
    
    println!("x is {}", x);
}

>>>x is 4
x is Hello
```




# Name Shadowing

Name shadowing is using the same variable names but from different scopes.

Before we were working inside the **same scope**. A *scope is basically some code between {}.*


```rust
fn main() {
    let x = 4;

    println!("x is {}", x);


    { let x =2;
    println!("x is: {}",x);
}
    let x = x+1;
    
    println!("x is {}", x);
}

>>> x is 4
x is 2
x is 5
```

Surprising right? We could have thought we would have obtain 4,2,3. But **because the second x is inside a different scope, that does not affect the x of the outter scope.**

I can access the x from the outter to the inner scope.

```rust

fn main() {
    let x = 4;

    println!("x is {}", x);


    { let x = x + 3;
    println!("x is: {}",x);
}
    let x = x+1;
    
    println!("x is {}", x);
}


>>>x is 4
x is 7
x is 5
```
Same way as before, even if we use a variable from the outter scope to the inner scope, the outter scope variable is not affected by the inner variable.


# Constants (**const**)

const means that value and type cannot be changed accross the script.
Just think about avogadro number or light speed. Those are constants and cannot be changed.
Even if we try to redefine the constant using const..., this will return an error.
In a script a **constant is defined once, an cannot be redefined/reassigned later or changed.**

*const CONSTANT_NAME_CONVENTION: type = value*

```RUST
fn main() {
    const SECONDS_IN_MINUTE: u32 = 60;

    println!("x is {}", SECONDS_IN_MINUTE);


}
>>> x is 60
```

