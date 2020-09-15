---
title: Degrees
tags: math,beginner
---

Converts an angle from radians to degrees.

- Use `math.Pi` and the radian to degree formula to convert the angle from radians to degrees.

```go
import "math"

func Degrees(r float64) float64 {
	return r * 180.0 / math.Pi
}
```

```go
Degrees(math.Pi / 2.0) // 90.0
```
