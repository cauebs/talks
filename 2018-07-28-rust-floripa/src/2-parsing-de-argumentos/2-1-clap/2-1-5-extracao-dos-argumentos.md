## Extração dos Argumentos

```rust
// Extrai o valor de `config`, se passado pelo usuário, senão usa "default.conf"
let config = matches.value_of("config").unwrap_or("default.conf");
println!("Value for config: {}", config);

// Chamar .unwrap() é seguro aqui, porque `INPUT` é necessário.
// Se `INPUT` não fosse obrigatório, poderia-se usar um `if let` para extrair o valor condicionalmente
println!("Using input file: {}", matches.value_of("INPUT").unwrap());

// A saída varia de acordo com quantas vezes o usuário passou a flag `verbose`.
// i.e. `myprog -v -v -v` or `myprog -vvv` vs `myprog -v`
match matches.occurrences_of("v") {
    0 => println!("No verbose info"),
    1 => println!("Some verbose info"),
    2 => println!("Tons of verbose info"),
    3 | _ => println!("Don't be crazy"),
}

// ...resto da lógica da aplicação
```

```shell
$ myprog --help
My Super Program 1.0
Kevin K. <kbknapp@gmail.com>
Does awesome things

USAGE:
    MyApp [FLAGS] [OPTIONS] <INPUT> [SUBCOMMAND]

FLAGS:
    -h, --help       Prints this message
    -v               Sets the level of verbosity
    -V, --version    Prints version information

OPTIONS:
    -c, --config <FILE>    Sets a custom config file

ARGS:
    INPUT    The input file to use

SUBCOMMANDS:
    help    Prints this message
    test    Controls testing features
```
