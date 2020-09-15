---
title: IsInRange
tags: math,beginner
---

Checks if the given number falls within the given range.

- Use `math.Min()` and `math.Max()` to determine the start and end of the range.
- Use arithmetic comparison to check if the given number is in the specified range.

```go
import "math"

func IsInRange(n, a, b float64) bool {
	s, e := math.Min(a, b), math.Max(a, b)
	return n >= s && n < e
}
```

```go
IsInRange(3, 2, 5) // true
IsInRange(2, 3, 5) // false
```
