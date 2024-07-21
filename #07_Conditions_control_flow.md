# Conditions and Control Flow

## Condition core operators
Make sure you are comparing the same types on each sides of the comparison.

- <
- >
- <=
- >=
- !=
- ==

**Basic Example**

```rust
fn main() {
    let cond = 2 <3;
    println!("{}",cond);
}
>>>true
```

```rust
fn main() {
    let cond = (2 as f32) <3.3;
    println!("{}",cond);
}
>>>True
```

# Compound Condition

Multiples conditions links with **logical operators such as and(&&), or(||), not(!).**



```rust
fn main() {
    let cond = (2 as f32) <3.3;
    let cond2 = true && cond;
    println!("{}",cond);
}

>>>true
```

Note: There is an importance order in compound condition like in math * before +.
In condition the order is ! > && > || 



# Control Flow (if/else if/else statements)
```rust
fn main() {
    let food = "cookie";
    if food != "cookie"{
        println!("I like cookies too");
    }else {
        println!("Oh Thats too bad")
    }
}
>>> Oh thats too bad
```


```rust
fn main() {
    let food = "Fruit";
    if food == "cookie"{
        println!("I like cookies too");
    } else if food =="Fruit"{
        println!("Thats Healthy")
    }else if food == "Bread"{
        println!("Miam")
}
    else {
        println!("Bad");
         
    }
}
>>>Heatlhy
```

