---
title: MapNumRange
tags: math,beginner
---

Maps a number from one range to another range.

- Returns `num` mapped between `oMin`-`oMax` from `iMin`-`iMax`.

```go
func MapNumRange(num, iMin, iMax, oMin, oMax float64) float64 {
	return ((num-iMin)*(oMax-oMin))/(iMax-iMin) + oMin
}
```

```go
MapNumRange(5.0, 0.0, 10.0, 0.0, 100.0) // 50.0
```
