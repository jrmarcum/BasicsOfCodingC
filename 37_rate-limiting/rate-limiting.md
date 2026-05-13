Go's rate limiter using a ticker channel is modeled with `sleep`. The first 5 requests sleep 200ms each; the burst batch sends the first 3 immediately and then rate-limits the remaining 2. Timestamps reflect actual run time.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running our program we see the first batch handled once every ~200ms. For the second batch we serve the first 3 immediately, then the remaining 2 with ~200ms delays.
___
##### Run Command:

`$ zig run -lc rate-limiting.c`

##### Results:

`request 1 2012-10-19 00:38:18.687438 +0000 UTC`
`request 2 2012-10-19 00:38:18.887471 +0000 UTC`
`request 3 2012-10-19 00:38:19.087238 +0000 UTC`
`request 4 2012-10-19 00:38:19.287338 +0000 UTC`
`request 5 2012-10-19 00:38:19.487331 +0000 UTC`
`request 1 2012-10-19 00:38:20.487578 +0000 UTC`
`request 2 2012-10-19 00:38:20.487645 +0000 UTC`
`request 3 2012-10-19 00:38:20.487676 +0000 UTC`
`request 4 2012-10-19 00:38:20.687483 +0000 UTC`
`request 5 2012-10-19 00:38:20.887542 +0000 UTC`
