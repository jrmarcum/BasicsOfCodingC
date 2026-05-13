Go's `sync.Mutex` maps directly to `CRITICAL_SECTION` on Windows and `pthread_mutex_t` on Unix. Three threads increment shared counters under the mutex; the result is always deterministic. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running the program shows that the counters updated as expected.
___
##### Run Command:

`$ zig run -lc mutexes.c`

##### Results:

`map[a:20000 b:10000]`
