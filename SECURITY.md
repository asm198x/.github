# Security policy

Asm198x is an assembler toolchain, so the realistic risks are crashes or
incorrect output when it's pointed at hostile or malformed input, rather than
remote compromise. Reports are still welcome.

## Reporting

Please report suspected vulnerabilities privately to **steve@stevehill.xyz**
rather than opening a public issue. Include the input and the steps to
reproduce.

This is a small project without a formal response window, but reports are read
and acted on. Once a fix ships, credit is given gladly — unless you'd rather
stay anonymous.

## Scope

In scope: the tools mishandling untrusted input (crashes, hangs, runaway memory)
or producing silently incorrect output. Out of scope: issues in dependencies
that are better reported upstream, and theoretical concerns without a
reproduction.
