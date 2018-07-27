## `?` no `main`

- `main` pode retornar `Return<(), E: Debug>`
- `?` pode ser usado como `unwrap`/`early return` em funções que retornam `Option` ou `Result`

```rust
use std::{fs, io};

fn main() -> Result<(), io::Error> {
    let contents = fs::read_to_string("file.txt");
    println!("{}", contents?);

    Ok(())
}
```
```shell
Error: Os { code: 2, kind: NotFound, message: "No such file or directory" }
```
