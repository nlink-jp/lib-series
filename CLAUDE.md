# CLAUDE.md — lib-series

**Organization rules (mandatory): https://github.com/nlink-jp/.github/blob/main/CONVENTIONS.md**

## Non-negotiable rules

- **Tests are mandatory** — write them with the implementation. A feature is not complete without tests.
- **Design for testability** — pure functions, injected dependencies, no untestable globals.
- **Zero external dependencies where possible** — standard library only. If external deps are needed, declare explicitly.
- **Docs in sync** — update `README.md` and `README.ja.md` in the same commit as behaviour changes.
- **Small, typed commits** — `feat:`, `fix:`, `test:`, `chore:`, `docs:`, `refactor:`, `security:`

## This series

Shared libraries for nlink-jp projects.

```
lib-series/
└── nlk/    github.com/nlink-jp/nlk   (Go — LLM utility toolkit)
```
