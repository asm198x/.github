# Asm198x

Modern, single-binary assembler/disassembler tooling for the retro CPUs of the 198x family. Asm198x provides source-compatible dialect front-ends, a shared declarative ISA-spec layer, spec-driven disassembly, and debug sidecars for emulator/tooling integration.

The goal is one documented, cross-platform toolchain surface across machines while preserving each platform's established source syntax where compatibility matters.

## Repositories

- **[asm198x](https://github.com/asm198x/asm198x)** — active Rust workspace: assembler engine and CLI, dialect front-ends, shared `isa` specs, `isa-disasm`, and `debug198x`.
- **[docs](https://github.com/asm198x/docs)** — documentation for the ISA spec format, Debug198x, and dialect references.

## Part of the 198x family

Asm198x owns the executable instruction-encoding layer for the 198x family. It complements the curriculum, emulator, asset-catalogue, and build-tools projects by making assembly, disassembly, and debug metadata available through stable tooling.
