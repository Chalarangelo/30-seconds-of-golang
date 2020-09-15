---
title: IntRange
tags: collection,math,beginner
---

Initializes an integer slice in the given range (inclusive).

- Use `make()` to create a slice of appropriate size.
- Use `range` to iterate over the slice and populate it.

```go
func IntRange(f, t, s int) []int {
	arr := make([]int, (t-f+1)/s)
	for i := range arr {
		arr[i] = i*s + f
	}
	return arr
}
```

```go
IntRange(0, 9, 2) // [0 2 4 6 8]
```
