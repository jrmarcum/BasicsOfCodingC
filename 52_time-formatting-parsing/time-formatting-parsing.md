C uses `strftime` for formatting and `sscanf` for parsing. Go's reference-time-based layouts (`"2006-01-02T15:04:05"`) are replaced with C's `strftime` format codes (`%Y-%m-%dT%H:%M:%S`). Sub-second precision uses `clock_gettime`.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc time-formatting-parsing.c`

##### Results:

`2014-04-15T18:00:15+00:00`
`2012-11-01 22:08:41 +0000 +0000`
`6:00PM`
`Tue Apr 15 18:00:15 2014`
`2014-04-15T18:00:15.161182+00:00`
`0000-01-01 20:41:00 +0000 UTC`
`2014-04-15T18:00:15-00:00`
`parsing time "8:41PM" as "%Y-%m-%dT%H:%M:%S": cannot parse`
___
#### Note: Dates and times will vary with each run.
___
