---
title: IsPowerOf2
tags: math,beginner
---

Returns `true` if the given number is a power of `2`, `false` otherwise.

- Use the bitwise binary AND operator (`&`) to determine if `n` is a power of `2`.
- Additionally, check that `n` is non-zero.

```go
func IsPowerOf2(n int) bool {
	return n > 0 && (n&(n-1)) == 0
}
```

```go
IsPowerOf2(0) // false
IsPowerOf2(1) // true
IsPowerOf2(8) // true
```
