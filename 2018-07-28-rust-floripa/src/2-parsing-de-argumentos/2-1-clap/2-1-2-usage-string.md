## Usage String

- Menos verboso
- Sacrifica alguma das configurações avançadas
- Implica em impacto _muito_ pequeno no desempenho em tempo de execução

```rust
extern crate clap;
use clap::{Arg, App, SubCommand};

let matches = App::new("myapp")
                      .version("1.0")
                      .author("Kevin K. <kbknapp@gmail.com>")
                      .about("Does awesome things")
                      .args_from_usage(
                          "-c, --config=[FILE] 'Sets a custom config file'
                          <INPUT>              'Sets the input file to use'
                          -v...                'Sets the level of verbosity'")
                      .subcommand(SubCommand::with_name("test")
                                  .about("controls testing features")
                                  .version("1.3")
                                  .author("Someone E. <someone_else@other.com>")
                                  .arg_from_usage("-d, --debug 'Print debug information'"))
                      .get_matches();
```
