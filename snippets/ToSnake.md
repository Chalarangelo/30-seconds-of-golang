---
title: ToSnake
tags: string,beginner
---

Converts a string to snake case.

- Use `strings.Fields()` to get the words in the string, `strings.Join()` to combine them using `"_"` as the separator.

```go
import "strings"

func ToSnake(s string) string {
	return strings.Join(strings.Fields(s), "_")
}
```

```go
ToSnake("some text") // "some_text"
```
