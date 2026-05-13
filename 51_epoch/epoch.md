C uses `clock_gettime(CLOCK_REALTIME, ...)` for nanosecond-precision Unix epoch values. Milliseconds are derived by dividing nanoseconds by 1,000,000.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc epoch.c`

##### Results:

`2012-10-31 16:13:58.292387000 +0000 UTC`
`1351700038`
`1351700038292`
`1351700038292387000`
`2012-10-31 16:13:58 +0000 UTC`
`2012-10-31 16:13:58.292387000 +0000 UTC`
___
#### Note: Dates and times will vary with each run.
___
