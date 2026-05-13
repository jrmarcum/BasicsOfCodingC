C has no interfaces. The closest idiom is a vtable: a struct of function pointers representing the required operations. Each concrete type provides its own implementations and a corresponding vtable instance.

___
##### Run Command:

`$ zig run -lc -lm interfaces.c`

##### Results:

`{3 4}`
`12`
`14`
`{5}`
`78.539816339745`
`31.415926535898`
