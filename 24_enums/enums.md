C enums are integer constants defined with `#define` or `enum`. The `String()` method is replaced by a `state_name()` lookup function; the `transition()` state machine uses a `switch` on `int` values.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc enums.c`

##### Results:

`connected`
`idle`
