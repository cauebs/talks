## `unwrap`/`expect`

```rust
use std::fs;

fn main() {
    let contents = fs::read_to_string("file.txt");
    println!("{}", contents.unwrap());
}
```
```shell
thread 'main' panicked at 'called `Result::unwrap()` on an `Err` value: Os { code: 2, kind: NotFound, message: "No such file or directory" }', libcore/result.rs:945:5
note: Run with `RUST_BACKTRACE=1` for a backtrace.
```

- `unwrap` deve ser usado com **muita** moderação.
- Se for usar, prefira sempre `expect`.
- Idealmente, deixe um comentário justificando o uso.
