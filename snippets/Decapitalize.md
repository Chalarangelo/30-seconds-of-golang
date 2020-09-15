---
title: Decapitalize
tags: string,beginner
---

Decapitalizes the first letter of a string.

- Use `strings.ToLower()` to decapitalize the first letter of the string.

```go
import "strings"

func Decapitalize(s string) string {
	return strings.ToLower(s[0:1]) + s[1:]
}
```

```go
Decapitalize("Boomerang") // "boomerang"
```
