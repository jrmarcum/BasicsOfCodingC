C uses `opendir`/`readdir` from `<dirent.h>` for directory listing, `mkdir`/`chdir` from `<unistd.h>` for creation and navigation, and a recursive `walk` function (sorted alphabetically) to replicate `filepath.Walk`.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc directories.c`

##### Results:

`Listing subdir/parent`
`  child true`
`  file2 false`
`  file3 false`
`Listing subdir/parent/child`
`  file4 false`
`Visiting subdir`
`  subdir true`
`  subdir/file1 false`
`  subdir/parent true`
`  subdir/parent/child true`
`  subdir/parent/child/file4 false`
`  subdir/parent/file2 false`
`  subdir/parent/file3 false`
