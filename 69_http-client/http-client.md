C uses raw TCP sockets for HTTP (via WinSock2 on Windows, POSIX sockets on Unix). The HTTP/1.0 GET request is sent manually; the response status and first 5 body lines are printed. HTTPS requires a TLS library such as OpenSSL.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc -lws2_32 http-client.c` (Windows)

`$ zig run -lc http-client.c` (Unix)

##### Results:

`Response status: 200 OK`
`<!DOCTYPE html>`
`<html>`
`  <head>`
`    <meta charset="utf-8">`
`    <title>Go by Example</title>`
