C uses `time.h` with `clock_gettime`/`gmtime` for time operations. Go's `time.Duration` string format (`25891h15m15.142266763s`) is reproduced manually. The fixed reference time is 2009-11-17 20:34:58.651387237 UTC (Unix 1258576498).
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc time.c`

##### Results:

`2012-10-31 15:50:13.793654000 +0000 UTC`
`2009-11-17 20:34:58.651387237 +0000 UTC`
`2009`
`November`
`17`
`20`
`34`
`58`
`651387237`
`UTC`
`Tuesday`
`true`
`false`
`false`
`25891h15m15.142266763s`
`25891.2542061852`
`1553475.25237111`
`93208515.1422267`
`93208515142266763`
`2012-10-31 15:50:13.793654000 +0000 UTC`
`2006-12-05 01:19:43.509120474 +0000 UTC`
___
#### Note: The current time (first line) and all derived duration/add values will vary with each run.
___
