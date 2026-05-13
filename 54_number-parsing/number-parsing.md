C uses `strtod`/`strtol`/`strtoul` from `<stdlib.h>` for number parsing. These functions accept a base argument and an end-pointer for error detection.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc number-parsing.c`

##### Results:

`1.234`
`123`
`456`
`789`
`135`
`strconv.Atoi: parsing "wat": invalid syntax`
