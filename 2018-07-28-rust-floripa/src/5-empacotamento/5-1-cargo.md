# Cargo

```shell
~ $ cargo new foo
     Created binary (application) `foo` project

~ $ exa -T foo
foo
├── Cargo.toml
└── src
   └── main.rs
```

```toml
[package]
name = "foo"
version = "0.1.0"
authors = ["Cauê Baasch de Souza <cauebs@pm.me>"]

[dependencies]
```

```shell
~/foo $ cargo run
   Compiling foo v0.1.0 (file:///home/cauebs/foo)
    Finished dev [unoptimized + debuginfo] target(s) in 0.39s
     Running `target/debug/foo`
Hello, world!
```

```shell
~/foo $ cargo publish
```

```shell
~ $ cargo install foo
```
