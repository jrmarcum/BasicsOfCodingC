C uses POSIX `regex.h` for regular expressions (`regcomp`/`regexec`/`regfree`). The API differs from Go's `regexp` package but produces identical results for these examples.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc regular-expressions.c`

##### Results:

`true`
`true`
`peach`
`[0 5]`
`[peach ea]`
`[0 5 1 3]`
`[peach punch pinch]`
`[[0 5 1 3] [6 11 7 9] [12 17 13 15]]`
`[peach punch]`
`true`
`p([a-z]+)ch`
`a <fruit>`
`a PEACH`
