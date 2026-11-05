# Phase 0 — Setup and C Warm-up

**Target dates:** November 4–17, 2026

## Objectives

- Establish a reliable Linux-based host development environment.
- Understand the roles of the compiler, debugger, build tool, and memory checker.
- Compile C with useful warnings and runtime sanitizers.
- Practice inspecting object sizes and memory addresses.

## Environment

Use Ubuntu under WSL2 for the host-based C exercises. VS Code should connect to that environment through Remote - WSL, so the terminal, compiler, debugger, and source files all refer to the same Linux environment.

Initial package setup:

```bash
sudo apt update
sudo apt install build-essential gdb make valgrind git
```

Check the tools:

```bash
gcc --version
gdb --version
make --version
valgrind --version
```

## Compiler baseline

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g main.c -o main
./main
```

For a separate sanitizer build:

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g \
    -fsanitize=address,undefined main.c -o main_san
./main_san
```

Use Valgrind on a normal debug build, not on a binary built with AddressSanitizer:

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g main.c -o main
valgrind --leak-check=full ./main
```

## Exercises

- [ ] `sizeof_demo`: inspect sizes of C types and objects.
- [ ] `memory_addresses`: print addresses and examine how pointers relate to objects.

Each exercise should include source code, build/run instructions, sample output, and a short explanation of what the output demonstrates.

## Completion criteria

Phase 0 is complete when the tools are verified, both warm-ups are implemented and understood, and the setup process plus any problems are recorded in the learning log.
