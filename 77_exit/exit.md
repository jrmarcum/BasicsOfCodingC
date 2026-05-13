C's `exit(3)` immediately terminates with status 3. Unlike Go's `os.Exit`, C's `exit()` does run `atexit` handlers (the C equivalent of deferred cleanup). The exit status is visible to the shell.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running `zig run -lc exit.c` exits with status 3. Unlike Go's `go run` which prints `exit status 3`, the shell shows nothing unless you check the exit code explicitly.
___
##### Run Command:

`$ zig run -lc exit.c ; echo $LASTEXITCODE` (PowerShell)

`$ zig run -lc exit.c ; echo $?` (Unix)

##### Results:

`3`
