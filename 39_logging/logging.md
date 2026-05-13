Go's `log` package (stderr, date/time prefix, file/line flag, custom prefix, buffer target) and `log/slog` JSON handler are replicated in C using `fprintf(stderr/stdout, ...)` with manual time formatting. Sample output; date and time will depend on when the example runs.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc logging.c`

##### Results:

`2023/08/22 10:45:16 standard logger`
`2023/08/22 10:45:16.904141 with micro`
`2023/08/22 10:45:16 logging.c:66: with file/line`
`my:2023/08/22 10:45:16 from mylog`
`ohmy:2023/08/22 10:45:16 from mylog`
`from buflog:buf:2023/08/22 10:45:16 hello`
`{"time":"2023-08-22T10:45:16.904166391-07:00","level":"INFO","msg":"hi there"}`
`{"time":"2023-08-22T10:45:16.904178985-07:00","level":"INFO","msg":"hello again","key":"val","age":25}`
