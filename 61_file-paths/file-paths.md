C has no `filepath` package. Path operations are implemented manually using string operations with `/` as the separator (POSIX-style). On Windows, `\` is also accepted by most file APIs.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc file-paths.c`

##### Results:

`p: dir1/dir2/filename`
`dir1/filename`
`dir1/filename`
`Dir(p): dir1/dir2`
`Base(p): filename`
`false`
`true`
`.json`
`config`
`t/file`
`../c/t/file`
