---
title: IsOdd
tags: math,beginner
---

Returns `true` if the given number is odd, `false` otherwise.

- Checks whether a number is odd or even using the modulo (`%`) operator.
- Returns `true` if the number is odd, `false` if the number is even.

```go
func IsOdd(n int) bool {
	return n % 2 == 1
}
```

```go
IsOdd(3) // true
```
