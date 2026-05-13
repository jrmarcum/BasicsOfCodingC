C uses `fopen`/`fread`/`fseek`/`ftell`/`fclose` from `<stdio.h>` for file I/O. `fgets` reads line-by-line. `fread` reads raw bytes. The `_ISSUE` suffix on this folder signals that it requires a pre-existing `./tmp/dat.txt` file to be created before running.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Create a new file with some data to read.
___
##### Run Command:

`$ echo hello > ./tmp/dat.txt`

`$ echo go >> ./tmp/dat.txt`

___
##### Run Command:

`$ zig run -lc reading-files.c`

##### Results:

`hello`
`go`
`5 bytes: hello`
`2 bytes @ 6: go`
`2 bytes @ 6: go`
`5 bytes: hello`
