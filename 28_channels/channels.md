C channels are modeled with a shared buffer plus a semaphore for synchronization. A sender thread writes the message and signals the semaphore; the receiver blocks on the semaphore before reading. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### When we run the program the `"ping"` message is successfully passed from one thread to another via our semaphore-backed channel.
___
##### Run Command:

`$ zig run -lc channels.c`

##### Results:

`ping`
