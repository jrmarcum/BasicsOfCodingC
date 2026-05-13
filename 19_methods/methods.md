C has no method syntax. Methods are expressed as free functions whose first parameter is a pointer (or value) of the struct type, following the `type_operation(struct, ...)` naming convention.

___
##### Run Command:

`$ zig run -lc methods.c`

##### Results:

`area:  50`
`perim: 30`
`area:  50`
`perim: 30`
