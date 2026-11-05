# Embedded C Foundations

A project-based learning repository for building the C, computer architecture, and firmware foundations needed for embedded systems.

**Roadmap:** November 2026 – June 2027  
**Current phase:** Phase 0 — Setup and C warm-up  
**Primary environment:** Ubuntu on WSL2, GCC, GDB, Make, Valgrind, and VS Code  
**Hardware track:** ESP32 / ESP-IDF work remains separate from the host-based C foundations exercises unless a phase explicitly connects them.

## Goals

- Understand C beyond syntax: memory, pointers, data representation, and undefined behavior.
- Become comfortable compiling, debugging, and testing C programs on Linux.
- Progress from host-based C exercises to bare-metal MCU programming.
- Build reusable low-level components and document the reasoning behind them.
- Finish with a robot-controller capstone that combines the concepts from the roadmap.

## Roadmap

| Phase | Focus | Target period |
|---|---|---|
| 0 | Development setup and C warm-up | Nov 4–17, 2026 |
| 1 | C memory and data representation | Nov 2026–Jan 2027 |
| 2 | STM32 registers and bare-metal GPIO | Jan–Feb 2027 |
| 3 | Interrupts, timers, and UART | Feb–Mar 2027 |
| 4 | Implementing a heap allocator | Mar–Apr 2027 |
| 5 | I2C and SPI | Apr–May 2027 |
| 6 | ARM and RISC-V architecture | May 2027 |
| 7 | Robot-controller capstone | May–Jun 2027 |

See [PROGRESS.md](PROGRESS.md) for the live checklist and [LEARNING_LOG.md](LEARNING_LOG.md) for dated notes.

## Repository layout

```text
.
├── README.md
├── PROGRESS.md
├── LEARNING_LOG.md
├── AI_HANDOFF.md
├── .gitignore
├── Phase_0_Setup/
├── Phase_1_C_Memory/
├── Phase_2_Bare_Metal/
├── Phase_3_Interrupts_UART/
├── Phase_4_Heap_Allocator/
├── Phase_5_I2C_SPI/
├── Phase_6_ARM_RISCV/
└── Phase_7_Robot_Capstone/
```

Each phase folder will contain its own notes, source code, and project-specific README files as work begins.

## Working conventions

1. Prefer small, testable commits with descriptive messages.
2. Explain the purpose of each program and the concepts it demonstrates.
3. Record compiler commands, expected output, observed output, and debugging steps.
4. Keep generated binaries and build directories out of Git.
5. Do not commit credentials, access tokens, private keys, or personal data.
6. Do not copy code into the repository without understanding and testing it.

## Build and debugging baseline

For a simple host-based C program:

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g main.c -o main
./main
```

When appropriate, use runtime sanitizers:

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g \
    -fsanitize=address,undefined main.c -o main_san
./main_san
```

Use GDB to inspect program execution and Valgrind to check supported Linux programs for memory errors and leaks. These tools complement tests; none proves a program is correct.

## Current status

The repository is initialized with the roadmap, tracking documents, and phase placeholders. Phase 0 is the active work area. Update the progress and learning log as tasks are completed.
