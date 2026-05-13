C uses `getenv`/`setenv` (POSIX) or `getenv`/`_putenv` (Windows) for environment variables. The global `environ` array lists all key=value pairs. `BAR` prints empty when unset since `getenv` returns `NULL`.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running the program shows that we pick up the value for `FOO` that we set in the program, but that `BAR` is empty.
___
##### Run Command:

`$ zig run -lc environment-variables.c`

##### Results:

`FOO: 1`
`BAR: `
`...`
___
#### The total list of keys in the environment will depend on your particular machine.
___
#### If we set `BAR` in the environment first, the running program picks that value up.
___
##### Run Command:

`$ $Env:BAR=2; ./environment-variables` (for Windows PowerShell)

`$ BAR=2 ./environment-variables` (for Unix-like environments)

##### Results:

`FOO: 1`
`BAR: 2`
`...`
