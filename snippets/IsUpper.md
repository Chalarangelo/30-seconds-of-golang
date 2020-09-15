---
title: IsUpper
tags: string,beginner
---

Checks if a string is upper case.

- Use `strings.ToUpper()` to convert the string to upper case and compare it to the original string.

```go
import "strings"

func IsUpper(s string) bool {
	return strings.ToUpper(s) == s
}
```

```go
IsUpper("GO") // true
IsUpper("Go") // false
```
