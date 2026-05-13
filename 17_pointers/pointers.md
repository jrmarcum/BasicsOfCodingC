___
#### `zeroval` doesn't change the `i` in `main`, but `zeroptr` does because it holds a pointer to the memory address of that variable.
___
##### Run Command:

`$ zig run -lc pointers.c`

##### Results:

`initial: 1`
`zeroval: 1`
`zeroptr: 0`
`pointer: 0x16b1234a4`
___
#### Note: The pointer address on the last line changes each time the program is run.
