---
title: Clamp
tags: math,beginner
---

Clamps `n` within the inclusive range specified by the boundary values `a` and `b`.

- If `n` falls within the range, return `n`.
- Otherwise, return the nearest number in the range.

```go
import "math"

func Clamp(n, a, b float64) float64 {
	return math.Max(math.Min(n, math.Max(a, b)), math.Min(a, b))
}
```

```go
Clamp(2.0, 3.0, 5.0) // 3.0
Clamp(1.0, -1.0, -5.0) // -1.0

```
