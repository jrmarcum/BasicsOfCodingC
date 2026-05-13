C has no built-in `flag` package. Flags are parsed manually from `argv`, supporting both `-flag=value` and `-flag value` syntax. Booleans are set by the presence of the flag name alone.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Try out the program by first giving it values for all flags.
___
##### Run Command:

`$ zig run -lc command-line-flags.c -- -word=opt -numb=7 -fork -svar=flag`

##### Results:

`word: opt`
`numb: 7`
`fork: true`
`svar: flag`
`tail: []`
___
#### Note that if you omit flags they automatically take their default values.
___
##### Run Command:

`$ zig run -lc command-line-flags.c -- -word=opt`

##### Results:

`word: opt`
`numb: 42`
`fork: false`
`svar: bar`
`tail: []`
___
#### Trailing positional arguments can be provided after any flags.
___
##### Run Command:

`$ zig run -lc command-line-flags.c -- -word=opt a1 a2 a3`

##### Results:

`word: opt`
`numb: 42`
`fork: false`
`svar: bar`
`tail: [a1 a2 a3]`
