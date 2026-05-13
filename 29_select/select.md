Go's `select` over multiple channels is modeled with per-channel semaphores. Each sender thread signals its semaphore after a delay; the receiver waits on each in arrival order. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### We receive the values `"one"` and then `"two"` as expected. The total execution time is only ~2 seconds since both sleeps run concurrently.
___
##### Run Command:

`$ zig run -lc select.c`

##### Results:

`received one`
`received two`
