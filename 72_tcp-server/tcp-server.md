C implements the TCP server using POSIX sockets (`socket`/`bind`/`listen`/`accept`). Each connection is handled in its own thread. The server reads one line, uppercases it, and sends back `ACK: UPPERCASE`. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Run the TCP server in the background, then send data and capture the response using netcat.
___
##### Run Command:

`$ zig run -lc -lws2_32 tcp-server.c &` (Windows)

`$ zig run -lc -lpthread tcp-server.c &` (Unix)
`$ echo "Hello from netcat" | nc localhost 8090`

##### Results:

`ACK: HELLO FROM NETCAT`
