---
title: MaxOf
tags: math,intermediate
---

Returns the maximum value of two or more numbers.

- Use `math.Inf(-1)` to set the initial maximum value to negative infinity.
- Use `range` and `math.Max()` to iterate over the numbers and get the maximum value.

```go
import "math"

func MaxOf(nums ...float64) float64 {
	max := math.Inf(-1)
	for _, num := range nums {
		max = math.Max(num, max)
	}
	return max
}
```

```go
MaxOf(3.0, 4.0, 2.0) // 4.0
```
