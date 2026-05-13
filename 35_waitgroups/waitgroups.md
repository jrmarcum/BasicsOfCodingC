Go's `sync.WaitGroup` maps to joining all threads after launch. Five threads run concurrently; each prints "starting" then sleeps 1 second then prints "done". The order of workers starting and finishing is nondeterministic. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### The order of workers starting up and finishing is likely to be different for each invocation.
___
##### Run Command:

`$ zig run -lc waitgroups.c`

##### Results:

`Worker 5 starting`
`Worker 3 starting`
`Worker 4 starting`
`Worker 1 starting`
`Worker 2 starting`
`Worker 4 done`
`Worker 1 done`
`Worker 2 done`
`Worker 5 done`
`Worker 3 done`
