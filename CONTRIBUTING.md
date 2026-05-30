# Contributing to Asm198x

Thanks for taking a look. Asm198x is a family of modern assemblers for retro
CPUs; it's early days, and help is welcome — especially from people who know a
machine's quirks first-hand.

This file applies to every repo in the [asm198x](https://github.com/asm198x)
org. The main one is [`asm198x`](https://github.com/asm198x/asm198x) (the Rust
workspace); [`docs`](https://github.com/asm198x/docs) holds the references.

## Build and check

```sh
cargo build
cargo test
cargo fmt --check
cargo clippy --workspace --all-targets -- -D warnings
```

All four must pass before a change lands. The workspace forbids `unsafe`, and
clippy denies `dbg_macro` and `unwrap_used` — so no stray `.unwrap()` or `dbg!`
in committed code. Keep library code free of panics; return errors instead.

## The accuracy bar

An assembler that emits the wrong bytes is worse than one that doesn't build, so
correctness of the instruction-set data is the highest bar:

- Opcodes, cycle counts, and affected flags go in the [`isa` spec](https://github.com/asm198x/asm198x/blob/main/crates/isa/src/) and **must come from a datasheet or primary source**. Cite the source in your PR.
- The spec's self-checking tests must stay green. Adding instructions or
  addressing modes? Add the encodings to the tests too.
- A good correctness fix comes with a test that pins the exact bytes.

## Dialect work

Each CPU's assembler aims to be **source-compatible with that machine's dominant
existing dialect** (6502 → ca65, and so on) — not a new house syntax. Before
adding or changing operand/directive syntax, read
[`decisions/syntax-stance.md`](https://github.com/asm198x/asm198x/blob/main/decisions/syntax-stance.md).
The dialect lives in the per-CPU parser; the shared encoding stays in `isa`.

## Commits and PRs

- Write clear, imperative commit subjects that describe the effect, and explain
  the *why* in the body. Conventional-commit prefixes (`feat:`, `fix:`) are
  welcome but not required.
- Keep changes focused — one concern per PR.
- Fill in the PR template's checklist.

## Reporting issues

Use the issue templates: a **bug report** (please include the source, the
command, and the expected vs actual bytes) or a **feature request**.
