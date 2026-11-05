# Memory Addresses Demo

## Goal

Practice observing object addresses and understanding the relationship between objects and pointers.

## Tasks

- [ ] Declare variables of different types and print their addresses with the correct format specifier.
- [ ] Store an object's address in a pointer of the matching type.
- [ ] Print the pointer value and the value obtained by dereferencing it.
- [ ] Compare addresses of array elements.
- [ ] Explain why pointer arithmetic advances in units of the pointed-to type rather than raw bytes.
- [ ] Use `%p` with an explicit cast to `(void *)` when printing an object pointer.

## Build

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g main.c -o memory_addresses
./memory_addresses
```

## Results

Add observed output and platform details after running the program. Address values can change between executions and should not be treated as fixed.

## Questions

- What is an object's address?
- What information does a pointer value represent?
- What does dereferencing a pointer mean?
- Why should an address printed in one run not be assumed to remain the same in another run?
