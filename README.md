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
