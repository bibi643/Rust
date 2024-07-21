# Functions Expressions and Statements Overview

- How to create/call/use them
- Statement vs expression
- Return value from function


# Functions (fn)
To name a function we have to use snake_case method -> test_one

Note: the function can be created anywhere in the script. Above or below the main function, it does not matter.

_fn name_function(paramaters){what to do when the function is called}_

```rust
fn main() {
    test_one();
    println!("Hello, world!");
}

fn test_one() {
    println!("test has been called")

}

>>>test has been called
Hello, world!
```

A function is made to reuse a piece of code.

```rust
fn main() {
    add_numbers(3,2);
    println!("Hello, world!");
}






fn add_numbers(x:i32, y:i32){
    println!("The sum is: {}", x + y)
}
>>> The sum is 5
```

Note: We could pass another parameter which does not have the same type.
add_numbers(x:i32, y:i32, z:f32) and it is ok.


# Statements VS Expressions
rust function can returns expressions but **cannot** return a Statement.
A Statement is something like _let x =20_. It does not evaluate anything it does not return anything.

An expression that evaluate something or return  something.
- println!
- function calls...
- 

```rust
fn main() {
    
    println!("Hello, world!");
    let number = {
        let x =3; //Expresion
        x+1 // NO ; means I return x +1 and put it inside number
    };
    println!("{}",number);
}
>>>4
```
If I put some x+1; I would have an error.


# Return values from Functions


fn main() {
    
    println!("Hello, world!");
   
    let result = add_numbers(32,45);
    println!("{}",result);
       
    }
    
fn add_numbers(x:i32, y:i32)-> i32{
    x + y 
}
```


To return something from a function we defined it and we add the type it will return using ->. And we write an expression at the very end of the function definition.
We can also use the keyword **return**. That's implies we can close the last expression with ;

```rust
fn main() {
    
    println!("Hello, world!");
   
    let result = add_numbers(32,45);
    println!("{}",result);
       
    }
    
fn add_numbers(x:i32, y:i32)-> i32{
    return x + y ;
}
>>>Hello, world!
77
```

## More complex examples

```rust
fn main() {
    
    println!("Hello, world!");
   
    let result = add_numbers(32,45);
    println!("{}",result);
       
    }
    




fn add_numbers(x:i32, y:i32)-> i32{
    let result = x + y;
    if result >10 {
        return result -10
    }
    result 
}
```
