Go's `context.Context` for HTTP request cancellation is modeled using a threaded HTTP server. Each connection handler runs in its own thread and sleeps 10 seconds; pressing Ctrl+C kills the server mid-request, demonstrating cancellation. On Unix, add `-lpthread` to the compile command.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Run the server in the background, then simulate a client request to `/hello`. Hit Ctrl+C shortly after to signal cancellation.
___
##### Run Command:

`$ zig run -lc -lws2_32 context.c &` (Windows)

`$ zig run -lc -lpthread context.c &` (Unix)
`$ curl localhost:8090/hello`

##### Results:

`server: hello handler started`
`^C`
`server: context canceled`
`server: hello handler ended`
