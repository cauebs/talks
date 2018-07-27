## Lidando com vários tipos de erros

```rust
use std::{error::Error, fs};

fn main() -> Result<(), Box<dyn Error>> {
    let contents = fs::read_to_string("file.txt");
    println!("{}", contents?);

    Ok(())
}
```
```shell
Error: Os { code: 2, kind: NotFound, message: "No such file or directory" }
```


```rust
pub trait Error: Debug + Display {
    fn description(&self) -> &str { ... }
    fn cause(&self) -> Option<&Error> { ... }
}
```
