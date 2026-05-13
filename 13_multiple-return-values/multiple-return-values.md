C does not support multiple return values. The idiomatic equivalent packs the values into a struct and returns that, or uses output pointer parameters for the extra values.

___
##### Run Command:

`$ zig run -lc multiple-return-values.c`

##### Results:

`3`
`7`
`7`
