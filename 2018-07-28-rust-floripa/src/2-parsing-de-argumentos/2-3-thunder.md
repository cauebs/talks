# Thunder

- Também usa macros pra gerar código que usa CLAP
- Expõe métodos como subcomandos
- Os argumentos são criados a partir dos parâmetros

```rust
struct MyApp;

#[thunderclap]
impl MyApp {
    /// Say hello to someone on the other side
    fn say_hello(name: &str, age: Option<u16>) { /* ... */ }

    /// It was nice to meet you!
    fn goodybe(name: Option<&str>) { /* ... */ }
}

fn main() {
    MyApp::start();
}
```
