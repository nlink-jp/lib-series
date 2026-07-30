# AGENTS.md — lib-series

## Project summary

Umbrella repository for nlink-jp's shared libraries consumed by tools in
other series. Each library lives in its own repository, included here as a
submodule. The catalog — one row per library — is [README.md](README.md);
this file covers only how to work with the umbrella (ADR-005).

## Key commands

| Command | Purpose |
|---------|---------|
| `git clone --recurse-submodules https://github.com/nlink-jp/lib-series.git` | Clone with all libraries |
| `git submodule update --init` | Populate submodules in an existing clone |
| `git submodule update --remote <lib>` | Pull a library's latest main |
| `git add <lib>` → commit `chore: bump <lib> to vX.Y.Z` | Update the pointer after a release |

## Gotchas

- Library development happens in the library repositories; new projects
  start in the workspace root `_wip/`, never directly inside this umbrella
  (CONVENTIONS.md — Starting a New Project).
- Submodule checkouts default to detached HEAD — `git checkout main` inside
  a submodule before committing.
- Submodule URLs are HTTPS only (SSH fails on machines without key auth).
- Consumers pin libraries by released version through the Go module proxy /
  PyPI-style resolution — never by `replace` directives pointing at local
  paths (org rule).
- Every submodule needs a catalog row in README.md — `check-org.sh` fails
  otherwise.

## Module path

Repository: `github.com/nlink-jp/lib-series`
