---
title: MinOf
tags: math,intermediate
---

Returns the minimum value of two or more numbers.

- Use `math.Inf(1)` to set the initial minimum value to positive infinity.
- Use `range` and `math.Min()` to iterate over the numbers and get the minimum value.

```go
import "math"

func MinOf(nums ...float64) float64 {
	min := math.Inf(1)
	for _, num := range nums {
		min = math.Min(num, min)
	}
	return min
}
```

```go
MinOf(3.0, 1.0, 2.0) // 1.0
```
