Go tickers are modeled with a loop that sleeps 500ms then prints the current timestamp. The ticker fires 3 times before being stopped. Timestamps reflect actual run time.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### The ticker ticks 3 times before we stop it. The timestamps reflect the actual run time.
___
##### Run Command:

`$ zig run -lc tickers.c`

##### Results:

`Tick at 2012-09-23 11:29:56.487625 -0700 PDT`
`Tick at 2012-09-23 11:29:56.988063 -0700 PDT`
`Tick at 2012-09-23 11:29:57.488076 -0700 PDT`
`Ticker stopped`
