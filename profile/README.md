# Asm198x

Modern, single-binary assemblers — and, in time, disassemblers — for the retro
CPUs of the 198x era. One consistent toolchain across machines, built to still
run in ten years.

The period assemblers are dead-OS binaries: you need DOSBox or a full emulator
just to invoke them. The modern community tools mostly work, but they're
scattered — a different program, syntax, and build dance per machine. Asm198x
aims to be one statically-linked, cross-platform, documented toolchain that
spans the family's CPUs, with each backend source-compatible with its machine's
established dialect so existing code still assembles.

It's early days, and built in the open.

## Repositories

- **[asm198x](https://github.com/asm198x/asm198x)** — the assembler workspace:
  the shared instruction-set spec and the assembler engine + CLI. 6502 first.
- **[docs](https://github.com/asm198x/docs)** — documentation: the spec format,
  per-machine dialect references.

## Part of the 198x family

A sibling project to retro-computing curriculum and emulator work that share a
hardware-reference layer. Assemblers, emulators, and teaching — three views of
the same machines.
