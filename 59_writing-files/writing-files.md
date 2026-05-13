C uses `fopen`/`fwrite`/`fflush`/`fclose` for file writing. `fflush` serves both the `Sync` and `Flush` roles. The `tmp/` directory must exist before running.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Try running the file-writing code.
___
##### Run Command:

`$ zig run -lc writing-files.c`

##### Results:

`wrote 5 bytes`
`wrote 7 bytes`
`wrote 9 bytes`
___
#### Then check the contents of the written files.
___
##### Run Command:

`$ cat ./tmp/dat1.txt`

##### Results:

`hello`
`go`
___
##### Run Command:

`$ cat ./tmp/dat2.txt`

##### Results:

`some`
`writes`
`buffered`
