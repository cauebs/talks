## Failure

```rust
extern crate failure;
#[macro_use] extern crate failure_derive;

use std::fmt

#[derive(Fail, Debug)]
struct MyError {
    code: i32,
    message: String,
}

impl fmt::Display for MyError {
    fn fmt(&self, f: &mut fmt::Formatter) -> fmt::Result {
        write!(f, "An error occurred with error code {}. ({})", self.code, self.message)
    }
}
```

```rust
extern crate failure;
#[macro_use] extern crate failure_derive;

#[derive(Fail, Debug)]
#[fail(display = "An error occurred with error code {}. ({})", code, message)]
struct MyError {
    code: i32,
    message: String,
}
```

```rust
extern crate failure;

use std::fs;

fn main() -> Result<(), failure::Error> {
    let contents = fs::read_to_string("file.txt");
    println!("{}", contents?);

    Ok(())
}
```
```shell
Error: Os { code: 2, kind: NotFound, message: "No such file or directory" }
```
