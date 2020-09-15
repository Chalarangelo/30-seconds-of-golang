---
title: RandIntSliceInRange
tags: math,random,intermediate
---

Returns a slice of `n` random integers in the specified range.

- Use `make()` to create an appropriate slice.
- Use `range` to iterate over the slice, `rand.Intn()` to generate random numbers between `0` and the distance between `min` and `max`, adding `min` to them.

```go
import "math/rand"

func RandIntSliceInRange(min, max, n int) []int {
	arr := make([]int, n)

	for i := range arr {
		arr[i] = rand.Intn(max-min) + min
	}
	return arr
}
```

```go
RandIntSliceInRange(12, 35, 10) // [19 34 29 15 25 21 18 23 32 27]
```
