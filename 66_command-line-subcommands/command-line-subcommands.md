C implements subcommand dispatch manually: check `argv[1]` for the subcommand name, then pass `argv[2..]` to per-subcommand flag parsers.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### First invoke the foo subcommand.
___
##### Run Command:

`$ zig run -lc command-line-subcommands.c -- foo -enable -name=joe a1 a2`

##### Results:

`subcommand 'foo'`
`  enable: true`
`  name: joe`
`  tail: [a1 a2]`
___
#### Now try bar.
___
##### Run Command:

`$ zig run -lc command-line-subcommands.c -- bar -level 8 a1`

##### Results:

`subcommand 'bar'`
`  level: 8`
`  tail: [a1]`
