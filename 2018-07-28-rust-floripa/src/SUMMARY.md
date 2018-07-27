# Summary

- [Introdução](./1-introducao/1-0-introducao.md)
    - [Domain Working Groups de 2018](./1-introducao/1-1-working-groups/1-1-0-working-groups.md)
        - [CLI WG](./1-introducao/1-1-working-groups/1-1-1-cli-wg.md)

    - [O que é uma CLI?](./1-introducao/1-2-o-que-e-cli.md)
    - [O que _não_ é uma CLI?](./1-introducao/1-3-0-o-que-nao-e-cli.md)
        - [TUI](./1-introducao/1-3-1-tui.md)
        - [GUI](./1-introducao/1-3-2-gui.md)

- [Parsing de Argumentos](./2-parsing-de-argumentos/2-0-parsing-de-argumentos.md)
    - [CLAP](./2-parsing-de-argumentos/2-1-clap/2-1-0-clap.md)
        - [Método 1: Builder Pattern](./2-parsing-de-argumentos/2-1-clap/2-1-1-builder-pattern.md)
        - [Método 2: Usage String](./2-parsing-de-argumentos/2-1-clap/2-1-2-usage-string.md)
        - [Método 3: YAML](./2-parsing-de-argumentos/2-1-clap/2-1-3-yaml.md)
        - [Método 4: Macro](./2-parsing-de-argumentos/2-1-clap/2-1-4-macro.md)
        - [Extração dos Argumentos](./2-parsing-de-argumentos/2-1-clap/2-1-5-extracao-dos-argumentos.md)

    - [StructOpt](./2-parsing-de-argumentos/2-2-structopt/2-2-0-structopt.md)
        - [Struct](./2-parsing-de-argumentos/2-2-structopt/2-2-1-struct.md)
        - [Enum](./2-parsing-de-argumentos/2-2-structopt/2-2-2-enum.md)

    - [Thunder](./2-parsing-de-argumentos/2-3-thunder.md)
    - [Docopt](./2-parsing-de-argumentos/2-4-docopt.md)
    - [std](./2-parsing-de-argumentos/2-5-std.md)

- [Tratamento de Erros](./3-tratamento-de-erros/3-0-tratamento-de-erros.md)
    - [`unwrap`/`expect`](./3-tratamento-de-erros/3-1-unwrap-expect.md)
    - [`?` no `main`](./3-tratamento-de-erros/3-2-no-main.md)
    - [Lidando com vários tipos de erros](./3-tratamento-de-erros/3-3-lidando-com-varios-tipos-de-erros.md)
    - [Failure](./3-tratamento-de-erros/3-4-failure.md)
    - [ExitFailure](./3-tratamento-de-erros/3-5-exitfailure.md)
    - [human-panic](./3-tratamento-de-erros/3-6-human-panic.md)

- [Testes](./4-testes.md)

- [Empacotamento](./5-empacotamento/5-0-empacotamento.md)
    - [Cargo](./5-empacotamento/5-1-cargo.md)
    - [Compilação Cruzada](./5-empacotamento/5-2-compilacao-cruzada.md)
    - [Geração de Pacotes](./5-empacotamento/5-3-geracao-de-pacotes.md)

- [Documentação](./6-documentacao.md)

- [Exemplos de sucesso](./7-exemplos/7-0-exemplos.md)
    - [exa](./7-exemplos/7-1-exa.md)
    - [ripgrep](./7-exemplos/7-2-ripgrep.md)
    - [fd](./7-exemplos/7-3-fd.md)
    - [bat](./7-exemplos/7-4-bat.md)
    - [tokei](./7-exemplos/7-5-tokei.md)
    - [hyperfine](./7-exemplos/7-6-hyperfine.md)
    - [durt](./7-exemplos/7-7-durt.md)

- [Fim](./8-fim.md)
