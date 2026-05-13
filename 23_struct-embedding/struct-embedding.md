C struct embedding is modeled with a named inner struct field. Methods on the inner type are called explicitly via the field name; the interface pattern is reproduced by calling the same function through a function pointer.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc struct-embedding.c`

##### Results:

`co={num: 1, str: some name}`
`also num: 1`
`describe: base with num=1`
`describer: base with num=1`
