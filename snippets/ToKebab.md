---
title: ToKebab
tags: string,beginner
---

Converts a string to kebab case.

- Use `strings.Fields()` to get the words in the string, `strings.Join()` to combine them using `"-"` as the separator.

```go
import "strings"

func ToKebab(s string) string {
	return strings.Join(strings.Fields(s), "-")
}
```

```go
ToKebab("some text") // "some-text"
```
