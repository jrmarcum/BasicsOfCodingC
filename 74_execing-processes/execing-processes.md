Go's `syscall.Exec` is C's `execvp` / `_execvp` — both replace the current process image with a new one. If the exec call succeeds, no code after it runs. The output is the result of `ls -a -l -h` in the lesson folder.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### When we run our program it is replaced by `ls`. Note: this example uses `execvp` which is available on both Unix and Windows (via `_execvp`).
___
##### Run Command:

`$ zig run -lc execing-processes.c`

##### Results:

`total 16`
`drwxr-xr-x  4 mark 136B Oct 3 16:29 .`
`drwxr-xr-x 91 mark 3.0K Oct 3 12:50 ..`
`-rw-r--r--  1 mark 1.3K Oct 3 16:28 execing-processes.c`
