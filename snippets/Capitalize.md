---
title: Capitalize
tags: string,beginner
---

Capitalizes the first letter of a string.

- Use `strings.ToUpper()` to capitalize the first letter of the string.

```go
import "strings"

func Capitalize(s string) string {
	return strings.ToUpper(s[0:1]) + s[1:]
}
```

```go
Capitalize("boomerang") // "Boomerang"
```
