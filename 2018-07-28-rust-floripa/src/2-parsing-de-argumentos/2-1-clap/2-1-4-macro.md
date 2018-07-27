## Macro

Abordagem híbrida: desempenho do _builder pattern_ sem o _boiler plate_.

```rust
#[macro_use]
extern crate clap;

let matches = clap_app!(myapp =>
    (version: "1.0")
    (author: "Kevin K. <kbknapp@gmail.com>")
    (about: "Does awesome things")
    (@arg CONFIG: -c --config +takes_value "Sets a custom config file")
    (@arg INPUT: +required "Sets the input file to use")
    (@arg debug: -d ... "Sets the level of debugging information")
    (@subcommand test =>
        (about: "controls testing features")
        (version: "1.3")
        (author: "Someone E. <someone_else@other.com>")
        (@arg verbose: -v --verbose "Print test information verbosely")
    )
).get_matches();
```
