---
title: ReverseString
tags: string,beginner
---

Reverses a string

- Use `make()` to create an appropriate `rune` slice.
- Use `range` and `len()` to iterate over the string's runes and add them in reverse to the result.
- Use `string()` to convert the `rune` slice to a `string`.

```go
func ReverseString(s string) string {
	o := make([]rune, len(s))
	for i, c := range s {
		o[len(s)-i-1] = c
	}
	return string(o)
}
```

```go
ReverseString("hello") // "olleh"
```
