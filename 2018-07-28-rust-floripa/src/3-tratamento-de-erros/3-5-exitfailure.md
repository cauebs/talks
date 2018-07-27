## ExitFailure

```rust
extern crate failure;

extern crate exitfailure;
use exitfailure::ExitFailure;

use std::{env, fs, io};

fn main() -> Result<(), ExitFailure> {
    let contents = fs::read_to_string("file.txt");
    println!("{}", contents?);

    Ok(())
}
```
```shell
Error: No such file or directory (os error 2)
```
