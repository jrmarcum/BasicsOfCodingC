C uses `getenv("TMPDIR"/"TMP"/"TEMP")` to locate the system temp directory, then builds unique names from `time()`+`rand()`. On POSIX systems `mkstemp`/`mkdtemp` can be used instead.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc temporary-files-and-directories.c`

##### Results:

`Temp file name: .../Temp/sample...`
`Temp dir name: .../Temp/sampledir...`
___
#### Note: Temp file and directory names will vary with each run.
___
