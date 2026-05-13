# Basics of Coding C — Project Context

## Purpose

Multi-language comparative study of programming syntax, language simplicity,
lines of code required, and compile/run performance. C is one of several
languages implemented against the same set of example programs, enabling
direct side-by-side comparison.

## Upstream Reference

Lessons are translated from **Basics of Coding Go** by Jon Marcum, which is
itself adapted from **Go by Example** by Mark McGranaghan. The upstream Go
content lives at `upstream/` in this repository and serves as the source of
truth for program logic and expected output.

- Upstream Go repo: https://github.com/jrmarcum/BasicsOfCodingGo
- Original Go by Example: https://github.com/mmcgrana/gobyexample

## Licensing Summary

This project contains two tiers of content with different licenses:

- **CC BY 3.0** — lesson files and code examples adapted from Basics of
  Coding Go (Jon Marcum) / Go by Example (Mark McGranaghan).
  License: http://creativecommons.org/licenses/by/3.0/

- **CC0 1.0** — original contributions by Jon Marcum (project structure,
  README, CLAUDE.md, comparative-study additions, and any lessons not derived
  from the above works). See LICENSE.

Attribution for all derived lesson content is centralized in NOTICE and in
the README Attribution/License sections. **Do NOT add per-file attribution
footers to lesson `.md` files** — this differs from BasicsOfCodingGo.

## Toolchain

C is compiled using `zig cc` (Zig's built-in C compiler), targeting C99.
This provides a single cross-platform toolchain consistent with other
languages in the comparative study.

Compile and run pattern:
```
$ zig run -lc filename.c
```

For programs that take command-line arguments (lessons 64–66), pass args
after the `--` separator:
```
$ zig run -lc command-line-arguments.c -- a b c d
```

For programs that link additional libraries:
```
$ zig run -lc -lm filename.c          # math (lessons 04, 20)
$ zig run -lc -lws2_32 filename.c     # Windows network (lessons 69–72)
$ zig run -lc -lpthread filename.c    # Unix threading (lessons 69–72)
```

## Project Structure

```
BasicsOfCodingC/
├── CLAUDE.md          — this file; canonical project context for Claude sessions
├── LICENSE            — CC0 (applies to Jon Marcum's original contributions)
├── NOTICE             — attribution notice for CC BY 3.0 derived content
├── README.md          — project overview, attribution section, license table
├── upstream/          — reference copy of BasicsOfCodingGo lessons
│   └── ##_topic-name/ — Go source and md for each lesson
└── ##_topic-name/
    ├── topic-name.c   — runnable C source for the lesson
    └── topic-name.md  — lesson explanation with run command and results
```

Lessons use two-digit prefixes (e.g., `01_hello-world`). All 78 lessons are
implemented (`01_hello-world` through `78_sha256-hashes`).

## C Translation Notes

Go features that have no direct C equivalent, and the idiomatic C approach:

| Go construct | C equivalent used |
|---|---|
| Slices | Struct with `data` pointer + `len` + `cap`, malloc/realloc |
| Maps | Simple struct arrays of key-value pairs (for small, fixed sets) |
| Multiple return values | Output parameters (`int *out`) or return struct |
| Closures | Struct capturing state + function pointer |
| Interfaces | Function pointer table (vtable pattern) |
| `defer` | Manual cleanup; `atexit()` for process-level cleanup |
| `goroutines` | OS threads: `CreateThread` (Win32) / `pthread_create` (Unix) |
| `channels` | Semaphore + shared buffer: Win32 semaphores / POSIX `sem_t` |
| `select` | Sequential `sem_timedwait` / `WaitForSingleObject` calls |
| `sync.WaitGroup` | `thread_join` loop after spawning all threads |
| `sync.Mutex` | `CRITICAL_SECTION` (Win32) / `pthread_mutex_t` (Unix) |
| `sync/atomic` | C11 `<stdatomic.h>`: `atomic_ullong`, `atomic_fetch_add` |
| `goroutines` / `channels` timeout | `sem_timedwait` (Unix) / `WaitForSingleObject(sem, ms)` (Win32) |
| `error` type | `int` return code with error message string |
| `panic` / `recover` | `setjmp`/`longjmp` with static `jmp_buf` and message |
| `range` over string | `for` loop with index, `(unsigned char)` cast for char values |
| `regexp` | POSIX `regex.h` (`regcomp`/`regexec`/`regfree`) |
| `net/http` client | Raw TCP socket: WinSock2 (Win32) / POSIX sockets (Unix) |
| `net/http` server | `bind`/`listen`/`accept` loop; `-lws2_32` on Windows |
| `text/template` | `strstr` substitution helpers (`tmpl_render`, `tmpl_if`, `tmpl_range`) |
| `os/exec` (exec) | `_execvp` (Win32) / `execvpe` (Unix) — replaces current process |
| `os/exec` (spawn) | `popen()` for stdout capture |
| `os/signal` | `signal(SIGINT, handler)` + `volatile int` flag polled in loop |
| SHA256 | Full FIPS 180-4 from scratch: `ROTR32` macro, 64 K constants, σ0/σ1/Σ0/Σ1/Ch/Maj |

## .gitignore

The project `.gitignore` covers:
```gitignore
# Compiled binaries produced by zig cc
*.exe
*.o
command-line-arguments
command-line-flags
command-line-subcommands
http-client
http-server
context
tcp-server

# Temporary files created by lesson examples
tmp/

# Zig compiler cache
.zig-cache/
zig-out/
```

## Notes for Future Claude Sessions

- Do **not** add per-file attribution footers to lesson `.md` files.
  Attribution is fully satisfied by README and NOTICE.
- The `58_reading-files_ISSUE` folder name signals a known issue — the
  lesson requires a `tmp/dat.txt` file to exist before running. The `tmp/`
  directory must be created manually before running lessons 58–60.
- Lessons 64–66 must be compiled to a binary before running, since they
  depend on command-line arguments that cannot be passed via `zig run`.
- Lessons 50–52 produce time-dependent output; the Results section in their
  `.md` files shows representative example output.
- For map-like structures (lesson 10), output is printed in insertion order
  (C has no hash map ordering guarantee); the note in the `.md` explains this.
- SHA1 (lesson 56), Base64 (lesson 57), and SHA256 (lesson 78) are implemented
  from scratch in C since the C standard library does not include these algorithms.
- Lessons 27–37 (concurrency) use OS threads: `CreateThread`/`CRITICAL_SECTION`/
  Win32 semaphores on Windows; `pthread_t`/`pthread_mutex_t`/`sem_t` on Unix.
  On Unix, add `-lpthread` to the compile command.
- Lesson 34 (atomic-counters) uses C11 `<stdatomic.h>` (`atomic_ullong`).
- Lessons 35–37 (waitgroups, worker-pools, rate-limiting) produce nondeterministic
  per-thread ordering; the `.md` files note this.
- Lessons 69–72 (http-client, http-server, context, tcp-server) use raw sockets.
  On Windows, compile with `-lws2_32`. On Unix, no extra flag needed.
- Lesson 74 (execing-processes) replaces the current process; output is from `ls`.
- Lesson 75 (spawning-processes) uses `popen()`; commands differ by platform.
- Lesson 76 (signals) requires sending SIGINT (Ctrl+C) at runtime; output includes
  a newline before "interrupt signal received".
- Lesson 32 (tickers) and 37 (rate-limiting) print timestamps that vary each run.
