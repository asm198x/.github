## What & why

<!-- What does this change, and why? Link any issue it closes (e.g. "Closes #12"). -->

## Type

- [ ] Bug fix (wrong bytes / crash / incorrect behaviour)
- [ ] New instruction, addressing mode, or directive
- [ ] New CPU / dialect
- [ ] Docs / tooling
- [ ] Other

## Checklist

- [ ] `cargo fmt --check` clean
- [ ] `cargo clippy --workspace --all-targets -- -D warnings` clean
- [ ] `cargo test` passes
- [ ] Tests added/updated — encodings pinned for any instruction or mode change
- [ ] Instruction-set facts cited from a datasheet / primary source (if `isa` changed)
- [ ] Docs updated (if behaviour or dialect changed)
