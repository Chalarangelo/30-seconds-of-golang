---
title: LCM
tags: math,recursion,intermediate
---

Returns the least common multiple of two or more numbers.

- Define a `gcd()` function that determines the greatest common divisor, using recursion.
- Use `gcd()` and the fact that `LCM(x, y) = x * y / GCD(x,y)` to determine the least common multiple.
- Use `range` to apply the calculation to all given numbers.


```go
func gcd(x, y int) int {
	if y == 0 {
		return x
	}
	return gcd(y, x%y)
}

func LCM(nums ...int) int {
	x := nums[0]
	for _, y := range nums[1:] {
		x = (x * y) / gcd(x, y)
	}
	return x
}
```

```go
LCM(12, 7) // 84
LCM([]int{1, 3, 4, 5}...) // 60
```
