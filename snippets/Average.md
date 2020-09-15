---
title: Average
tags: math,beginner
---

Returns the average of two or more numbers.

- Use `range` to iterate over the values of `nums`, adding each value to `sum`.
- Return the result of dividing `sum` with `len(nums)`.

```go
func Average(nums ...float64) float64 {
	sum := float64(0)
	for _, num := range nums {
		sum += num
	}
	return sum / float64(len(nums))
}
```

```go
Average(1.0, 4.0) // 2.5
Average([]float64{1.0, 2.0, 3.0}...) // 2.0
```
