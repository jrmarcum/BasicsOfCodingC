Go's `signal.NotifyContext` is modeled with C's `signal()` handler. The handler sets a flag when `SIGINT` or `SIGTERM` arrives; the main loop polls the flag. Pressing Ctrl+C sends `SIGINT` and causes the program to exit.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### When we run this program it will block waiting for a signal. By typing `ctrl-C` (which the terminal shows as `^C`) we can send a `SIGINT` signal, causing the program to print the cancellation cause and then exit.
___
##### Run Command:

`$ zig run -lc signals.c`

##### Results:

`awaiting signal`
`^C`
`interrupt signal received`
`exiting`
