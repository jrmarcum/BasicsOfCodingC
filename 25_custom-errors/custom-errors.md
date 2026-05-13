C custom errors use a struct carrying error fields. Type-checked matching (`errors.As`) is replaced by returning the struct directly via an output pointer and checking the return code.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc custom-errors.c`

##### Results:

`42`
`can't work with it`
