# sizeof Demo

## Goal

Explore the `sizeof` operator and observe the sizes of selected C types and objects on the current platform.

## Tasks

- [ ] Print the size of `char`, `short`, `int`, `long`, `long long`, `float`, `double`, and selected pointer types.
- [ ] Create variables and print the size of each variable using `sizeof`.
- [ ] Compare the size of an array with the size of a pointer to its first element.
- [ ] Use `sizeof array / sizeof array[0]` to calculate an array's element count while the array is still an array expression.
- [ ] Explain why observed sizes are platform- and implementation-dependent where the C standard permits variation.

## Build

```bash
gcc -std=c11 -Wall -Wextra -Wpedantic -g main.c -o sizeof_demo
./sizeof_demo
```

## Results

Add your compiler/platform details and observed output here after running the program.

## Questions

- What does `sizeof` return?
- Why is `sizeof(char)` always 1 in C, even if a byte is not eight bits on every conceivable implementation?
- Why does an array's `sizeof` differ from a pointer's `sizeof`?
