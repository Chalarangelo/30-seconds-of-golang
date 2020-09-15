---
title: GCD
tags: math,recursion,intermediate
---

Calculates the greatest common divisor between two or more numbers.

- Define a `gcd()` function for two numbers, which uses recursion.
- Base case is when `y` equals `0`, which returns `x`.
- Otherwise the GCD of `y` and the remainder of the division `x/y` is returned.
- Use `gcd()` and `range` to apply the calculation to all given numbers.

```go
func gcd(x, y int) int {
	if y == 0 {
		return x
	}
	return gcd(y, x%y)
}

func GCD(nums ...int) int {
	r := nums[0]
	for _, num := range nums[1:] {
		r = gcd(r, num)
	}
	return r
}
```

```go
GCD(8, 36) // 4
GCD([]int{12, 8, 32}...) // 4
```
