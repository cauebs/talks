## Builder Pattern

- Permite configurações mais avançadas (inclusive gerar argumentos dinamicamente)
- Muito verboso

```rust
extern crate clap;
use clap::{Arg, App, SubCommand};

let matches = App::new("My Super Program")
                      .version("1.0")
                      .author("Kevin K. <kbknapp@gmail.com>")
                      .about("Does awesome things")
                      .arg(Arg::with_name("config")
                          .short("c")
                          .long("config")
                          .value_name("FILE")
                          .help("Sets a custom config file")
                          .takes_value(true))
                      .arg(Arg::with_name("INPUT")
                          .help("Sets the input file to use")
                          .required(true)
                          .index(1))
                      .arg(Arg::with_name("v")
                          .short("v")
                          .multiple(true)
                          .help("Sets the level of verbosity"))
                      .subcommand(SubCommand::with_name("test")
                                  .about("controls testing features")
                                  .version("1.3")
                                  .author("Someone E. <someone_else@other.com>")
                                  .arg(Arg::with_name("debug")
                                      .short("d")
                                      .help("print debug information verbosely")))
                      .get_matches();
```
