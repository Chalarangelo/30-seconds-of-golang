---
title: IndentString
tags: string,beginner
---

Indents each line in the provided string.

- Use `strings.Replace()` to prepend `i` to each line.

```go
import "strings"

func Indent(s, i string) string {
	return i + strings.Replace(s, "\n", "\n"+i, -1)
}
```

```go
Indent("Lorem\nIpsum","_") // "_Lorem\n_Ipsum"
```
