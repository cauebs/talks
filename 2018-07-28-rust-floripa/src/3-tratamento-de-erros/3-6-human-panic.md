## human-panic

Se tudo falhar...

```rust
#[macro_use]
extern crate human_panic;

fn main() {
   setup_panic!();

   println!("A normal log message");
   panic!("OMG EVERYTHING IS ON FIRE!!!")
}
```
Sem `human-panic`
```shell
thread 'main' panicked at 'OMG EVERYTHING IS ON FIRE!!!', examples/main.rs:2:3
note: Run with `RUST_BACKTRACE=1` for a backtrace.
```

**Com** `human-panic`
```
Well, this is embarrassing.

human-panic had a problem and crashed.
To help us diagnose the problem you can send us a crash report.

We have generated a report file at "/var/folders/zw/bpfvmq390lv2c6gn_6byyv0w0000gn/T/report-8351cad6-d2b5-4fe8-accd-1fcbf4538792.toml".
Submit an issue or email with the subject of "human-panic Crash Report" and include the report as an attachment.

- Homepage: https://github.com/yoshuawuyts/human-panic
- Authors: Yoshua Wuyts <yoshuawuyts@gmail.com>

We take privacy seriously, and do not perform any automated error collection.
In order to improve the software, we rely on people to submit reports.

Thank you kindly!
```
