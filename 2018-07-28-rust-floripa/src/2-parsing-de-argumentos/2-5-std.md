# std

- Para tarefas simples, ferramentas simples

```rust
use std::env;

for argument in env::args() {
    println!("{}", argument);
}

for (key, value) in env::vars() {
    println!("{}: {}", key, value);
}

let key = "HOME";
match env::var(key) {
    Ok(val) => println!("{}: {:?}", key, val),
    Err(e) => println!("couldn't interpret {}: {}", key, e),
}
```
