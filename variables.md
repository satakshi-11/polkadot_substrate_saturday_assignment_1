BINDING AND MUTABILITY

1.
```
fn main() {
    let x: i32 = 5; 
    let y: i32; 

    assert_eq!(x, 5);
    println!("Success!");
}

output: Success!

solution :initialise x

```
2.
```
fn main() {
    let mut x =  1;
    x += 2; 
    
    assert_eq!(x, 3);
    println!("Success!");
}

output: Success!

solution: add mut since x is used twice

```
SCOPE

3.
```
fn main() {
    let x: i32 = 10;
    
    {
        let y: i32 = 5;
        println!("The value of x is {} and value of y is {}", x, y);
    }
    println!("The value of x is {}", x); 
}

output:
The value of x is 10 and value of y is 5
The value of x is 10

solution: Remove y in the last println 

```
4.
```
fn main() {
    let x = define_x();
    println!("{}, world", x); 
}

fn define_x() -> String{
    let x = "hello".to_string();
    x
}

output: hello, world

solution: add to_string() and declare x in main fn

```

SHADOWING

5.
```
fn main() {
    let x: i32 = 5;
    {
        let x = 12;
        assert_eq!(x, 12);
    }

    assert_eq!(x, 5);

    let x =  42;
    println!("{}", x); // Prints "42".
}

output: 42

solution: changed the value in (x,_)

```
6.
```
fn main() {
    let mut x: i32 = 1;
    x = 7;
    // Shadowing and re-binding
    let x = x; 
    let y = 4;
    // Shadowing
    let y = "I can also be bound to text!"; 

    println!("Success!");
}

output: Success!

solution: remove unwanted fields

```
UNUSED VARIABLES

7.
```
fn main() {
    let x = 1;
    println!("{}",x)
}

output: 1

solution:use variable with println

```

DESTRUCTURING

8.
```
fn main() {
    let (mut x, y) = (1, 2);
    x += 2;
    assert_eq!(x, 3);
    assert_eq!(y, 2);
    println!("Success!");
}

output: Success!

solution: added mut in x

```

DESTRUCTURING ASSIGNMENTS

9.
```

fn main() {
    let (x, y);
    (x,..) = (3, 4);
    [.., y] = [1, 2];
    // Fill the blank to make the code work
    assert_eq!([x,y], [3,2]);
    println!("Success!");
} 

output: Success!

solution: add [3,2]

```