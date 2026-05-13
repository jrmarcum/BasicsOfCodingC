Go's `exec.Command` is modeled with C's `popen`, which spawns a subprocess and returns a pipe to its stdout. The spawned programs return output that is the same as running them directly. Output depends on the current environment.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### The spawned programs return output as if run directly from the command-line. Output will vary by platform and environment.
___
##### Run Command:

`$ zig run -lc spawning-processes.c`

##### Results:

`> date`
`Thu 05 May 2022 10:10:12 PM PDT`
`command exit rc = 1`
`> grep hello`
`hello grep`
`> ls -a -l -h`
`drwxr-xr-x  4 mark 136B Oct 3 16:29 .`
`drwxr-xr-x 91 mark 3.0K Oct 3 12:50 ..`
`-rw-r--r--  1 mark 1.3K Oct 3 16:28 spawning-processes.c`
