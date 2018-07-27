## Struct

```rust
#[macro_use]
extern crate structopt;
use structopt::StructOpt;

use std::path::PathBuf;

#[derive(StructOpt, Debug)]
#[structopt(name = "example", about = "An example of StructOpt usage.")]
struct Opt {

    /// Activate debug mode
    #[structopt(short = "d", long = "debug")]
    debug: bool,

    /// Set speed
    #[structopt(short = "s", long = "speed", default_value = "42")]
    speed: f64,

    /// Input file
    #[structopt(parse(from_os_str))]
    input: PathBuf,

    /// Output file, stdout if not present
    #[structopt(parse(from_os_str))]
    output: Option<PathBuf>,

}

fn main() {
    let opt = Opt::from_args();
    println!("{:?}", opt);
}
```
