C uses integer return codes and output pointer parameters for error handling rather than multiple return values. A custom error struct carries additional context, mirroring Go's custom error types.

___
##### Run Command:

`$ zig run -lc errors.c`

##### Results:

`f1 worked: 10`
`f1 failed: can't work with 42`
`f2 worked: 10`
`f2 failed: 42 - can't work with it`
`42`
`can't work with it`
