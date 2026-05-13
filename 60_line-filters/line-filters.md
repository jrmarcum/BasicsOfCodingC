C reads stdin with `fgets` in a loop, applying `toupper` from `<ctype.h>` to each character. The `ferror` check mirrors Go's `scanner.Err()`.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### To try out our line filter, first make a file with a few lowercase lines. If "lines.txt" file exists delete it before doing the exercise.
___
##### Run Command:

`$ echo hello   > ./tmp/lines.txt`

`$ echo filter >> ./tmp/lines.txt`

___
#### Then use the line filter to get uppercase lines.
___
##### Run Command:

`$ cat ./tmp/lines.txt | zig run -lc line-filters.c`

##### Results:

`HELLO`
`FILTER`
