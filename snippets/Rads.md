---
title: Rads
tags: math,beginner
---

Converts an angle from degrees to radians.

- Use `math.Pi` and the degree to radian formula to convert the angle from degrees to radians.

```go
import "math"

func Rads(d float64) float64 {
	return d * math.Pi / 180.0
}
```

```go
Rads(90.0) // ~1.5708
```
