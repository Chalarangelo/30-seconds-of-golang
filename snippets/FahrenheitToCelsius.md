---
title: FahrenheitToCelsius
tags: math,beginner
---

Converts Fahrenheit to Celsius.

- Follows the conversion formula `C = (F - 32) * 5/9`.

```go
func FahrenheitToCelsius(d float64) float64 {
	return (d - 32.0) * 5.0 / 9.0
}
```

```go
FahrenheitToCelsius(32.0) // 0.0
```
