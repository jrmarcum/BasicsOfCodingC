C uses `rand()`/`srand()` from `<stdlib.h>` for pseudorandom numbers. The default seed is 1 (deterministic until explicitly seeded). Note: C's seeded-42 sequence differs from Go's since each runtime uses its own PRNG algorithm.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc random-numbers.c`

##### Results:

`81,87`
`0.131538`
`7.123187,8.434115`
`0,28`
`38,7`
`38,7`
___
#### Note: Numbers will vary per run (except lines 5 and 6 which are seeded with 42 and will be consistent per platform).
___
