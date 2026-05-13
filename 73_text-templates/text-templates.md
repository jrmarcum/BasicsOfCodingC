Go's `text/template` `{{.}}`, `{{if}}`, and `{{range}}` actions are replicated with a minimal C template engine: `strstr` locates `{{.}}` and substitutes the value; `if`/`range` dispatch with dedicated helpers.
___
#### To run the program, make sure you are in the program's folder, then use the Run Command below.
___
##### Run Command:

`$ zig run -lc text-templates.c`

##### Results:

`Value: some text`
`Value: 5`
`Value: [Go Rust C++ C#]`
`Name: Jane Doe`
`Name: Mickey Mouse`
`yes `
`no `
`Range: Go Rust C++ C# `
