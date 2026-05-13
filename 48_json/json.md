C has no built-in JSON library. Encoding is done via `printf`/`snprintf`, and decoding uses simple string-searching helpers. For production use, a library like cJSON or jansson would replace these helpers.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc json.c`

##### Results:

`true`
`1`
`2.34`
`"vector"`
`["apple","peach","pear"]`
`{"apple":5,"lettuce":7}`
`{"Page":1,"Fruits":["apple","peach","pear"]}`
`{"page":1,"fruits":["apple","peach","pear"]}`
`map[num:6.13 strs:[a b]]`
`6.13`
`a`
`{1 [apple peach]}`
`apple`
`{"apple":5,"lettuce":7}`
