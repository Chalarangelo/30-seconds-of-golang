---
title: Concat
tags: collection,beginner
---

Concatenates two slices.

- Implement an appropriate function for each type.
- Use `append()` and the fact that it's a variadic function to concatenate the slices.

```go
func ConcatInt(a,b []int) []int {
	return append(a, b...)
}
func ConcatFloat64(a,b []float64) []float64 {
	return append(a, b...)
}
func ConcatBool(a,b []bool) []bool {
	return append(a, b...)
}
func ConcatStrings(a,b []string) []string {
	return append(a, b...)
}
```

```go
ConcatStrings([]string{"a", "b", "c"}, []string{"d", "e"}) // [a b c d e]
```
