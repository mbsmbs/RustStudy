# RustStudy
Study Rust Programming Language

A binary can be generated using Rust compiler : rustc
in terminal :
```
$ rustc filename.rs
```

Then execute : 
```
$ ./filename
```

# 1. Hello World

```
fn main()
{
    println!("Hello World!!");
}
```

# 2. Comments
```
// This is a single line comment
/* 
This is 
a multiple lines
comments 
*/
```

# 3. Formatted print
```
println!("{} days", 31);

println!("{0}, this is {1}, {1}, this is {0}", "Alice", "Bob");

println!("{subject} {verb} {object}",
           object = "the lazy dog",
           subject = "the quick brown fox",
           verb = "jumps over");
           
println!("{} of {:b} people know binary, the other half doesn't", 1, 2);    // binary

println!("{number:>width$}", number=1, width=6);    // 5 white spaces + 1

println!("{number:>0width$}", number=1, width=6);   // 000001

println!("My name is {0}, {1} {0}", "Bond", "James");
```

## 3-1. Formatting-Debug
```
#[derive(Debug)]
struct Structure(i32);

#[derive(Debug)]
struct Deep(Structure);

fn main() {
    println!("{:?} months in a year.", 12);                     // {:?} similar {} // 12 months in a year.
    println!("{1:?} {0:?} is the {actor:?} name.",              
             "Slater",
             "Christian",
             actor="actor's");                                  // "Christian" "Slater" is the "actor\'s" name.

    println!("Now {:?} will print!", Structure(3));             // Now Structure(3) will print!
    
    println!("Now {:?} will print!", Deep(Structure(7)));       // Now Deep(Structure(7)) will print!
}
```

- Pretty printing with {:#?}

```
#[derive(Debug)]
struct Person<'a> {
    name: &'a str,
    age: u8
}

fn main() {
    let name = "Peter";
    let age = 27;
    let peter = Person { name, age };

    // Pretty print
    println!("{:#?}", peter);
}

// Person {
    name: "Peter",
    age: 27,
   }
```
