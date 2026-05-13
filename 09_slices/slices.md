C has no built-in slice type. This lesson implements a dynamic string array struct with `len` and `cap` fields to mirror Go slice behavior, using `malloc`/`realloc` for growth.

___
##### Run Command:

`$ zig run -lc slices.c`

##### Results:

`emp: [  ]`
`set: [a b c]`
`get: c`
`len: 3`
`apd: [a b c d e f]`
`cpy: [a b c d e f]`
`sl1: [c d e]`
`sl2: [a b c d e]`
`sl3: [c d e f]`
`dcl: [g h i]`
`2d:  [[0] [1 2] [2 3 4]]`
