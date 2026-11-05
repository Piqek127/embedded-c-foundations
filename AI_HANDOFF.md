# AI Handoff

This file is the shared context for AI-assisted work on this repository. Update it when the project state changes significantly so another assistant can continue without guessing.

## Project

Embedded C Foundations — November 2026 to June 2027.

## Learning approach

- Teach from first principles and explain why mechanisms work.
- Prefer a substantial project goal over disconnected toy exercises.
- Do not dump a complete solution when guided reasoning or a smaller example would teach more.
- Review the learner's implementation and explain defects before proposing a rewrite.
- Separate verified facts from assumptions.
- For MCU-specific behavior, check the exact device documentation and toolchain details.
- Keep a record of commands, environment details, test results, and unresolved questions.

## Roadmap

1. Phase 0: setup and C warm-up.
2. Phase 1: C memory and data representation.
3. Phase 2: STM32 registers and bare-metal GPIO.
4. Phase 3: interrupts, timers, and UART.
5. Phase 4: implementing a heap allocator.
6. Phase 5: I2C and SPI.
7. Phase 6: ARM and RISC-V architecture.
8. Phase 7: robot-controller capstone.

See `PROGRESS.md` for the detailed checklist and target periods.

## Current state (2026-11-05)

- Phase 0 is active.
- Repository structure and tracking files have been initialized.
- Planned host development environment: Ubuntu on WSL2 with GCC, GDB, Make, and Valgrind.
- VS Code is the intended editor, using Remote - WSL for the Ubuntu environment.
- Existing ESP32 / ESP-IDF work is a separate learning track for now; do not mix its environment into the WSL host-C setup without a specific reason.

## Collaboration protocol

When handing work between assistants:

1. Read this file, `PROGRESS.md`, and the relevant project README.
2. Inspect the actual source before making claims about implementation.
3. State the exact file and line or function being discussed when possible.
4. Give reproducible commands for build and test.
5. Report what was changed, what was tested, and what remains uncertain.
6. Do not overwrite another assistant's work without inspecting it first.
7. Do not commit secrets or personal information.

## Latest handoff

**Status:** Repository initialized; Phase 0 setup verification and warm-up tasks remain.

**Next recommended task:** Verify the WSL2 Ubuntu toolchain, then create and compile the first `sizeof` demonstration.

**Unresolved:** Actual installed tool versions and WSL2 setup status have not yet been recorded.
