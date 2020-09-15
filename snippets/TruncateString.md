---
title: TruncateString
tags: string,beginner
---

Truncates a string up to a specified length.

- Use `len()` to determine if the length is greater than `l`.
- Return the string truncated to the desired length, with `"..."` appended to the end or the original string.

```go
func TruncateString(s string, l int) string {
	r := s
	if len(s) > l {
		if l > 3 {
			l -= 3
		}
		r = s[0:l] + "..."
	}
	return r
}
```

```go
TruncateString("boomerang", 7); // "boom..."
```
