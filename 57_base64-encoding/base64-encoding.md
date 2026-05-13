C has no built-in base64 library. Standard and URL-safe base64 are implemented from scratch. The URL-safe variant replaces `+` with `-` and `/` with `_`.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### The string encodes to slightly different values with the standard and URL base64 encoders (trailing `+` vs `-`) but they both decode to the original string as desired.
___
##### Run Command:

`$ zig run -lc base64-encoding.c`

##### Results:

`YWJjMTIzIT8kKiYoKSctPUB+`
`abc123!?$*&()'-=@~`

`YWJjMTIzIT8kKiYoKSctPUB-`
`abc123!?$*&()'-=@~`
