# Basics of Coding C
## Preface
What this text is and what it is not: This text is intended to introduce the reader to the basics of the C programming language in the sense that they will be able to write minimal types of programs and run the code. It is not intended to go into advanced topics like concurrency, advanced data structures, object-oriented programming, testing and debugging techniques, and other software engineering principals.

The programs are intended to be run in the terminal as that is common to most operating systems. Linux and Mac come preinstalled with a terminal. Windows may or may not have it pre-installed. "Windows Terminal" can be installed from the Microsoft Store.

## Installation and Setup of Zig (to compile and run C)
To setup Zig for use, navigate to the [ziglang](https://github.com/ziglang/zig/wiki/Install-Zig-from-a-Package-Manager) website and locate an appropriate package manager for your operating system. Install and follow the directions on how to perform further settings for use. A package manager makes the install process much easier (brew for Mac, chocolatey for Windows, and varies based on linux distribution). If Zig has been installed properly you will be able to type the following command in the terminal command line and receive the response shown:
```
$ zig version
0.13.0
(Note: the version shown here varies with your installed version)
```
Zig ships with a built-in C compiler (`zig cc`) that supports C99 and later. All examples in this project run with a single command:
```
$ zig run -lc filename.c
```
The `-lc` flag links the C standard library. A few lessons require additional flags:

- **Math** (lessons 04, 20): `zig run -lc -lm filename.c`
- **Windows network** (lessons 69–72): `zig run -lc -lws2_32 filename.c`
- **Unix threading** (lessons 69–72): `zig run -lc -lpthread filename.c`
- **Command-line args** (lessons 64–66): `zig run -lc filename.c -- arg1 arg2 ...`

## Comments
Comments are used to document what your code does so that others can understand it when reviewing your code.
```c
// This is a single-line comment
/* This is a
   multi-line comment */
```

## Keywords
|          |          |          |            |          |
|:--------:|:--------:|:--------:|:----------:|:--------:|
| auto     | break    | case     | char       | const    |
| continue | default  | do       | double     | else     |
| enum     | extern   | float    | for        | goto     |
| if       | inline   | int      | long       | register |
| restrict | return   | short    | signed     | sizeof   |
| static   | struct   | switch   | typedef    | union    |
| unsigned | void     | volatile | while      | _Bool    |

## Data Types
> ### 1. Basic Types
>> #### a. **char**: single character or small integer, 1 byte
>> #### b. **short**: short integer, 2 bytes
>> #### c. **int**: integer, typically 4 bytes
>> #### d. **long**: long integer, at least 4 bytes
>> #### e. **long long**: long long integer, at least 8 bytes
>> #### f. **float**: single-precision floating point, 4 bytes
>> #### g. **double**: double-precision floating point, 8 bytes
>> #### h. **long double**: extended-precision floating point
> ### 2. Derived Types
>> #### a. **Pointers**: hold memory addresses of another variable
>> #### b. **Arrays**: fixed-size sequence of elements of the same type
>> #### c. **Structs**: collection of variables of different types grouped under a single name
>> #### d. **Unions**: similar to struct but members share the same memory
>> #### e. **Enums**: named integer constants
> ### 3. **void**: absence of a type; used for functions that return nothing or generic pointers

## Operators
> ### Arithmetic Operators
> |        |                                                    |
> |:------:|:---------------------------------------------------|
> | **+**  | add one number to another                          |
> | **-**  | subtract one number from another                   |
> | **\*** | multiply one number by another                     |
> | **/**  | divide one number by another                       |
> | **%**  | remainder of dividing one number by another        |
> | **++** | increase the value of a variable by 1              |
> | **--** | decrease the value of a variable by 1              |
> ### Comparison Operators
> |        |                                                         |
> |:------:|:--------------------------------------------------------|
> | **==** | check if a variable is equal to another                 |
> | **!=** | check if a variable is not equal to another             |
> | **>**  | check if a variable is greater than another             |
> | **<**  | check if a variable is less than another                |
> | **>=** | check if a variable is greater than or equal to another |
> | **<=** | check if a variable is less than or equal to another    |
> ### Logical Operators
> |        |                                                 |
> |:------:|:------------------------------------------------|
> | **&&** | returns true if both statements are true        |
> | **\|\|** | returns true if one of the statements is true |
> | **!**  | reverse the result of a true or false statement |
> ### Assignment Operators
> |         |                                                                        |
> |:-------:|:-----------------------------------------------------------------------|
> | **=**   | assign a value to a variable                                           |
> | **+=**  | add a number to the existing value and assign the result               |
> | **-=**  | subtract a number from the existing value and assign the result        |
> | **\*=** | multiply the existing value by a number and assign the result          |
> | **/=**  | divide the existing value by a number and assign the result            |
> | **%=**  | take the remainder of the existing value divided by a number           |

## Statements
A statement is an instruction that a program can execute.
> ### Conditional Statements
> | **if**        | performs a statement if a condition is met                                           |
> | **if-else**   | performs a statement if a condition is met, otherwise performs the else statement    |
> | **switch**    | selects one of many code blocks to execute based on an expression                   |
> ### Iterative Statements
> | **for**       | loop with initial, condition, and increment expressions                 |
> | **while**     | loop that continues while a condition is true                          |
> | **do-while**  | executes the body at least once, then continues while condition is true |
> ### Transfer Statements
> | **break**     | terminates the enclosing loop or switch statement            |
> | **continue**  | skips the rest of the loop body and continues to next iteration |
> | **goto**      | sends control flow to a labeled statement                    |
> | **return**    | returns a value from a function                              |

## Functions
> ### 1. **main**: entry point of every C program
> ### 2. **printf / fprintf**: formatted output
> ### 3. **scanf / fscanf**: formatted input
> ### 4. **malloc / calloc / realloc / free**: dynamic memory management

## File Input and Output
> ### 1. File Input
>> #### a. fopen, fread, fgets, fscanf
>> #### b. Error handling with NULL check and errno
> ### 2. File Output
>> #### a. fopen, fwrite, fputs, fprintf
>> #### b. fclose, fflush

## Attribution

This project is adapted in part from **[Basics of Coding Go](https://github.com/jrmarcum/BasicsOfCodingGo)**
by [Jon Marcum](https://github.com/jrmarcum), licensed under the
[Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).

Basics of Coding Go was itself adapted in part from **[Go by Example](https://github.com/mmcgrana/gobyexample)**
by [Mark McGranaghan](https://github.com/mmcgrana), also licensed under the
[Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/).

Attribution for all derived lesson content is centralized in this README and in the NOTICE file.
This project exists as a platform for multi-language comparative study of syntax, language
simplicity, lines of code required, and compile/run performance.

## License

This repository contains two tiers of content:

| Content | License |
| --- | --- |
| Lesson files and code examples adapted from *Basics of Coding Go* (derived from *Go by Example*) | [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/) — see NOTICE |
| Original contributions by Jon Marcum (project structure, README, CLAUDE.md, comparative study additions) | [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) — see LICENSE |

The root `LICENSE` file (CC0) applies to Jon Marcum's original contributions only.
The `NOTICE` file clarifies that CC BY 3.0 governs all content adapted from *Basics of Coding Go*
and *Go by Example*.
