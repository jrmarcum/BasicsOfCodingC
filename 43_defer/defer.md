C has no `defer` keyword. Cleanup is called explicitly after the main work completes, or via a `goto cleanup` label for early-exit paths. The create → write → close ordering matches Go's deferred execution.

___
#### Create the `tmp` directory first if it does not exist.
___
##### Run Command:

`$ mkdir -p tmp`

`$ zig run -lc defer.c`

##### Results:

`creating`
`writing`
`closing`
