# Data Types

# Primitive Data Types


Definition:

Primitive data type are the basic or **fundamental data types used to declare a variable**

- Primitive
- Scalar: int, boolean...

Is something that has a finite set of possible values, following some scale, each value can be compared to any other value as either equal, greater or less.



- Compound: tuple, array
a composite data type or compound data type is any data  type which can be constructed in a program using the programming language primitive data types and other composite types



## Scalar
### Signed and unsigned integers (i32, u32)
- i32 (default)
- i8
- i16
- i64
- i128

  integer means it can be positive or negative numbers -> **signed integer**

**uint** is for **unsigned** integer, so the integer has to be positive.
- u32 (default)
- u8
- ...


```rust
let a: i32 = -21
let x: u32 = 972
```

### Range number by byte selection (binary)
u8 and i8 has the same number of bytes but the range of number that can deal with is different due to the signed/unsigned property.


u8 goes from 0 to 2^8 -1 (because it is unsigned), 0 ->255.
i8 goes from -2^7 to 2^-1, -128 to 127.

### Floating points (f32, f64)
- f32 (single precision)
- f64 (double precision)

```rust

let floatin_pts: f32 =10.32
```

### Boolean (bool)

True or False
0 or 1.

let t_or_f: bool = false
let t_or_f: bool = true

let t_or_f: bool = 0
let t_or_f: bool = 1


### Charracters type (char)
Note we use char and **single quotation marks.**
let letter: char = 'a'
let punct: char = ':'


## Compound type

### Tuples: ()

#### Basics

**Fix length of sequence of element that is immutable.**

```rust
let tup:(i32,bool,char) = (1,true, 's')
let tup2: (i8, bool, char) = (1, true, 's')

```

We can obviously make them mutuable as previously mentionned.
 _let mut tup:(i32,bool,char) = (1,true,'w')_

#### How to access tuple elements?

```rust
fn main() {
    let tup: (i32,bool,char) =(1,true,'s')
    Println!("{}",tup);
    
}
>>>Println!("{}",tup);
  |                  ^^^ `(i32, bool, char)` cannot be formatted with the default formatter

```

So to **access the element of a tuple, we use indexes.**

```rust
fn main() {
    let tup: (i32,bool,char) =(1,true,'s');
    println!("{}",tup.1);
    }
>>>true
```


#### Changing the tuple

First let's make it mutuable using mut.

```rust
fn main() {
    let mut tup: (i32,bool,char) =(1,true,'s');
    tup.0= 23;

    println!("{}",tup.0);
    }
>>>23
```


### Arrays: []
The elements inside the array have to have the same type (all int, all floats...)
In rust the arrays are defined by the type of the datas and the number of datas.
arr here is made of 5 elements i32 types. I cannot add new datas in this array. I would have to create a new one or redifine it.
```rust
let arr: [i32,5]= [1,2,3,4,5]
```


#### Access the element
Same as tuple, using indexing.

```rust
fn main() {
    let arr = [1,2,3,4,5];
    println!("x is :{}",arr[0]);

    
    }
>>>1
```



#### Modifify the array




