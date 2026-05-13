C has no built-in test runner. A lightweight test framework is implemented by hand: each `Test*` function runs assertions and reports pass/fail. The output format mirrors Go's `go test -v` output including subtests and timing.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc testing-and-benchmarking.c`

##### Results:

`=== RUN   TestIntMinBasic`
`--- PASS: TestIntMinBasic (0.00s)`
`=== RUN   TestIntMinTableDriven`
`=== RUN   TestIntMinTableDriven/0,1`
`=== RUN   TestIntMinTableDriven/1,0`
`=== RUN   TestIntMinTableDriven/2,-2`
`=== RUN   TestIntMinTableDriven/0,-1`
`=== RUN   TestIntMinTableDriven/-1,0`
`--- PASS: TestIntMinTableDriven (0.00s)`
`    --- PASS: TestIntMinTableDriven/0,1 (0.00s)`
`    --- PASS: TestIntMinTableDriven/1,0 (0.00s)`
`    --- PASS: TestIntMinTableDriven/2,-2 (0.00s)`
`    --- PASS: TestIntMinTableDriven/0,-1 (0.00s)`
`    --- PASS: TestIntMinTableDriven/-1,0 (0.00s)`
`PASS`
`ok  	testing-and-benchmarking	0.023s`
