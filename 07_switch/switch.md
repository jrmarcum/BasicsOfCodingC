C has no type-switch construct; that section uses a tagged-union pattern instead. C `switch` cases fall through by default; `break` is required to prevent fall-through.

___
##### Run Command:

`$ zig run -lc switch.c`

##### Results:

`Write 2 as two`
`It's a weekday`
`It's after noon`
`I'm a bool`
`I'm an int`
`Don't know type string`
___
#### Note: The weekday line and time-of-day line will reflect the actual day and time when the program is run.
