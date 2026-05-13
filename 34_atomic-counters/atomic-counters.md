Go's `sync/atomic` maps to C11's `<stdatomic.h>`. Fifty threads each increment an `atomic_ullong` 1000 times using `atomic_fetch_add`. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### We expect to get exactly 50,000 operations. Had we used a plain `int` with `ops++`, we'd likely get a different number between runs due to data races.
___
##### Run Command:

`$ zig run -lc atomic-counters.c`

##### Results:

`ops: 50000`
