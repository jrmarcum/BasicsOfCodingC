C has no closure syntax. The closest idiom is a heap-allocated state struct passed to a function, giving each "closure" its own independent captured state.

___
##### Run Command:

`$ zig run -lc closures.c`

##### Results:

`1`
`2`
`3`
`1`
