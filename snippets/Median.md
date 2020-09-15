---
title: Median
tags: math,intermediate
---

Returns the median of a collection of numbers.

- Find the midpoint and convert it to an integer, use `sort.Float64s()` to sort the given numbers.
- Return the number at the midpoint if length is odd, otherwise the average of the two middle numbers.

```go
import (
	"math"
	"sort"
)

func Median(nums ...float64) float64 {
	m, n := int(math.Floor(float64(len(nums))/2.0)),
		nums[:]
	sort.Float64s(n)

	if len(nums)%2 == 0 {
		return (n[m] + n[m+1]) / 2.0
	}
	return n[m]
}
```

```go
Median(5.0, 6.0, 50.0, 1.0, -5.0) // 5.0
```
