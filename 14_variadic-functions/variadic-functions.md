C supports variadic functions via `<stdarg.h>`. Unlike Go, the caller must pass the argument count explicitly since C has no way to determine it automatically.

___
##### Run Command:

`$ zig run -lc variadic-functions.c`

##### Results:

`[1 2] 3`
`[1 2 3] 6`
`[1 2 3 4] 10`
