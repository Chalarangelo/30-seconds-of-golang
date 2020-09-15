---
title: ToCamel
tags: string,intermediate
---

Converts a string to kebab case.

- Use `range` and `strings.Fields()` to iterate over the words in the string.
- Use `strings.ToUpper()` and `strings.ToLower()` to capitalize the first letter of each word and lowercase the rest.

```go
import "strings"

func ToCamel(s string) string {
	c := ""
	for _, w := range strings.Fields(s) {
		c += strings.ToUpper(w[0:1]) + strings.ToLower(w[1:])
	}
	return strings.ToLower(c[0:1]) + c[1:]
}
```

```go
ToCamel("some text") // "someText"
```
