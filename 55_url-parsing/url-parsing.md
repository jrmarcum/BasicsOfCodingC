C has no built-in URL parsing library. We implement a minimal parser for the format `scheme://user:pass@host:port/path?query#fragment` using string operations.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running our URL parsing program shows all the different pieces that we extracted.
___
##### Run Command:

`$ zig run -lc url-parsing.c`

##### Results:

`postgres`
`user:pass`
`user`
`pass`
`host.com:5432`
`host.com`
`5432`
`/path`
`f`
`k=v`
`map[k:[v]]`
`v`
