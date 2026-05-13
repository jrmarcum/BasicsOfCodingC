C has no built-in crypto library. SHA1 is implemented from scratch using the standard FIPS 180-4 algorithm with `regcomp`/`regexec` equivalents replaced by bit-manipulation in 512-bit chunks.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running the program computes the hash and prints it in a human-readable hex format.
___
##### Run Command:

`$ zig run -lc sha1-hashes.c`

##### Results:

`sha1 this string`
`cf23df2207d99a74fbe169e3eba035e633b65d94`
