---
title: Sum
tags: math,beginner
---

Returns the sum of two or more numbers.

- Use `range` to iterate over the values of `nums`, adding each value to `sum`.

```go
func Sum(nums ...float64) float64 {
	sum := float64(0)
	for _, num := range nums {
		sum += num
	}
	return sum
}
```

```go
Sum(1.0, 4.0) // 5.0
Sum([]float64{1.0, 2.0, 3.0}...) // 6.0
```
