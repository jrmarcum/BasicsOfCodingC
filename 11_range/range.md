C has no `range` keyword; for loops with explicit indices replace all `range` forms. Key-value iteration uses parallel arrays. String iteration yields the byte index and the byte value (matching Go's ASCII rune values for the ASCII subset).

___
##### Run Command:

`$ zig run -lc range.c`

##### Results:

`sum: 9`
`index: 1`
`a -> apple`
`b -> banana`
`key: a`
`key: b`
`0 103`
`1 111`
