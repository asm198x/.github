# Asm198x — org container

This folder is the org container for the **`asm198x` GitHub organisation**. It is not a Git repo; each child folder is an independent repo with its own remote. Commit inside the repo that owns the file.

Asm198x is the third sibling of the 198x family — a family of modern,
single-binary assemblers and disassemblers for retro CPUs — peer to Code198x
(curriculum) and Emu198x (emulator). See the umbrella context at
[`../CLAUDE.md`](../CLAUDE.md) and the binding architecture decision at
[`../decisions/asm198x-and-shared-isa-spec.md`](../decisions/asm198x-and-shared-isa-spec.md).

## Repos in this org

| Folder | GitHub repo | Role |
|--------|-------------|------|
| [`asm198x/`](asm198x/) | `asm198x/asm198x` | **Flagship workspace.** The Rust workspace: the `isa` spec crate + the `asm198x` engine/CLI. Start here for assembler work; it has its own [`CLAUDE.md`](asm198x/CLAUDE.md) and `decisions/`. |
| [`.github/`](.github/) | `asm198x/.github` | Org profile (`profile/README.md`) and shared community-health files. |
| [`docs/`](docs/) | `asm198x/docs` | Documentation — the spec format, dialect references. |
| [`asm198x.github.io/`](asm198x.github.io/) | `asm198x/asm198x.github.io` | Public site (Astro, GitHub Pages via Actions). House style mirrors the family sites. |

## Working here

- **Commit in the right subfolder.** Each repo is independent; `git status` from
  the container shows nothing (it isn't a repo).
- **Cross-project decisions** live in the umbrella [`../decisions/`](../decisions/);
  Asm198x-only decisions live in [`asm198x/decisions/`](asm198x/decisions/).
- **Hardware facts** come from the umbrella primary library
  [`../reference/`](../reference/) and [`../syntheses/`](../syntheses/), per
  [`../decisions/shared-hardware-reference-canon.md`](../decisions/shared-hardware-reference-canon.md).
