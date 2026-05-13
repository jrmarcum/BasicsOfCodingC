C provides `argc`/`argv` as the direct equivalents of Go's `os.Args`. `argv[0]` is the program name; arguments start at `argv[1]`.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
___
##### Run Command:

`$ zig run -lc command-line-arguments.c -- a b c d`

##### Results:

`[/path/to/tmp/command-line-arguments a b c d]`
`[a b c d]`
`c`
