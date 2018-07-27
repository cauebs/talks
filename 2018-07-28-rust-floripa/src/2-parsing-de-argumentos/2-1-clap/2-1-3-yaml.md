## YAML

- Mantém o código Rust mais limpo
- Facilita a internacionalização
- Adiciona mais dependências à crate
- Tem um impacto um pouco maior no desempenho em tempo de execução

```yml
name: myapp
version: "1.0"
author: Kevin K. <kbknapp@gmail.com>
about: Does awesome things
args:
    - config:
        short: c
        long: config
        value_name: FILE
        help: Sets a custom config file
        takes_value: true
    - INPUT:
        help: Sets the input file to use
        required: true
        index: 1
    - verbose:
        short: v
        multiple: true
        help: Sets the level of verbosity
subcommands:
    - test:
        about: controls testing features
        version: "1.3"
        author: Someone E. <someone_else@other.com>
        args:
            - debug:
                short: d
                help: print debug information
```

```rust
#[macro_use]
extern crate clap;
use clap::App;

let yaml = load_yaml!("cli.yml");
let matches = App::from_yaml(yaml).get_matches();
```
