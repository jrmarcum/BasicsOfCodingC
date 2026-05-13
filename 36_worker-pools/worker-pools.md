Go's goroutine worker pool with channels is modeled using threads and a mutex-protected job counter. Three worker threads pull jobs from a shared counter until all 5 jobs are claimed. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### The program shows the 5 jobs being executed by various workers. It takes about 2 seconds despite doing 5 seconds of total work because 3 workers run concurrently.
___
##### Run Command:

`$ zig run -lc worker-pools.c`

##### Results:

`worker 1 started  job 1`
`worker 2 started  job 2`
`worker 3 started  job 3`
`worker 1 finished job 1`
`worker 1 started  job 4`
`worker 2 finished job 2`
`worker 2 started  job 5`
`worker 3 finished job 3`
`worker 1 finished job 4`
`worker 2 finished job 5`
