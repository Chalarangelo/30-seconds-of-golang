---
title: RandIntInRange
tags: math,random,beginner
---

Returns a random integer in the specified range.

- Use `rand.Intn()` to generate a random number between `0` and the distance between `min` and `max` and add `min` to it.

```go
import "math/rand"

func RandIntInRange(min, max int) int {
	return rand.Intn(max-min) + min
}
```

```go
RandIntInRange(0, 5) // 2
```
