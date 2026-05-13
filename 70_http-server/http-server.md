C implements the HTTP server using raw TCP sockets. The server handles `GET /hello` (returns `hello\n`) and `GET /headers` (echoes request headers). Handlers are dispatched by inspecting the request line.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Run the server in the background, then access the `/hello` route with curl.
___
##### Run Command:

`$ zig run -lc -lws2_32 http-server.c &` (Windows)

`$ zig run -lc http-server.c &` (Unix)
`$ curl localhost:8090/hello`

##### Results:

`hello`
