C has no `panic` keyword. The equivalent is `fprintf(stderr, ...)` followed by `abort()` (raises SIGABRT, non-zero exit) or `exit(1)`. C error handling prefers explicit return codes over panicking.

___
##### Run Command:

`$ zig run -lc panic.c`

##### Results:

`panic: a problem`
`Aborted`
___
#### Note: The exact abort message varies by OS and C runtime. The program always exits with a non-zero status.
