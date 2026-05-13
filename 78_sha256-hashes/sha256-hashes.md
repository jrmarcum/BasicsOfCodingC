C implements SHA256 from scratch following FIPS 180-4: ROTR32 macros, 64 round constants, message schedule expansion, and 64-round compression. The C standard library has no SHA256; this mirrors the SHA1 approach from lesson 56.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
#### Running the program computes the hash and prints it in a human-readable hex format.
___
##### Run Command:

`$ zig run -lc sha256-hashes.c`

##### Results:

`sha256 this string`
`1af1dfa857bf1d8814fe1af8983c18080019922e557f15a8a0d3db739d77aacb`
