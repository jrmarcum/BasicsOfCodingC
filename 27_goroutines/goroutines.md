C goroutines are modeled with OS threads (`CreateThread` on Windows, `pthread_create` on Unix). The direct call runs synchronously; the two threads run concurrently and may interleave their output. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### When we run this program, we see the output of the blocking call first, then the output of the two threads. The threads' output may be interleaved, because they run concurrently.
___
##### Run Command:

`$ zig run -lc goroutines.c`

##### Results:

`direct : 0`
`direct : 1`
`direct : 2`
`goroutine : 0`
`going`
`goroutine : 1`
`goroutine : 2`
`done`
