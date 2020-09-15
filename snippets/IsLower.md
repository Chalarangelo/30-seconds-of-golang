---
title: IsLower
tags: string,beginner
---

Checks if a string is lower case.

- Use `strings.ToLower()` to convert the string to lower case and compare it to the original string.

```go
import "strings"

func IsLower(s string) bool {
	return strings.ToLower(s) == s
}
```

```go
IsUpper("go") // true
IsUpper("Go") // false
```
