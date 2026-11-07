# lib-series

Shared libraries for [nlink-jp](https://github.com/nlink-jp) projects.

## Libraries

| Library | Lang | Description |
|---------|------|-------------|
| [mailparse](https://github.com/nlink-jp/mailparse) | Go | Reads .eml, Outlook .msg and winmail.dat (TNEF) composed by an attacker into one shape — header order and duplicates kept, addresses parsed before display names are decoded, every repair, guess or cut a warning, limits shared across nested messages. MS-CFB (exported as `cfb`), compressed RTF and TNEF read in-house; depends only on `golang.org/x/text` and `golang.org/x/net` |
| [mermaid-render](https://github.com/nlink-jp/mermaid-render) | Go | Go library that turns mermaid source into an image — flowcharts, ER and sequence diagrams on a white card, read as mermaid 12.0.0 reads them. Built so terminal agents can show diagrams in their transcripts; a diagram it cannot draw right is refused and shown as source |
| [nlk](https://github.com/nlink-jp/nlk) | Go | Lightweight LLM utility toolkit — guard, jsonfix, strip, backoff, validate. Zero external dependencies |
| [nlk-py](https://github.com/nlink-jp/nlk-py) | Python | Python edition of nlk — same 5 modules, same API design. Zero external dependencies |
| [pathguard](https://github.com/nlink-jp/pathguard) | Go | One judgement of whether a path may be touched — system locations, credential stores, agent configuration, a server's own directories — compared by file identity as well as by name; `pathguard/workdir` carries the ADR-021 work-directory contract. Zero external dependencies |
| [toml](https://github.com/nlink-jp/toml) | Go | TOML 1.1.0 decoder that replaces BurntSushi/toml in the organization's tools — strict by default (a key the struct does not know is an error, listed with its full name), field matching as BurntSushi does, passes the toml-test suite. Zero external dependencies |
