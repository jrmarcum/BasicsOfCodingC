C has no generics. The generic `SlicesIndex` is implemented as a concrete `slices_index` for `const char*`; the generic `List[T]` is implemented as a concrete `int_list` singly-linked list.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc generics.c`

##### Results:

`index of zoo: 2`
`list: [10 13 23]`
