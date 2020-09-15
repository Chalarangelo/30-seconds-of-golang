---
title: Digits
tags: math,intermediate
---

Converts an integer to an array of digits.

- Use `strconv.Itoa()` to convert the given number to a string, `make()` and `len()` to create an appropriate slice.
- Use `range` in combination with `strings.Split()` to iterate over the digits, converting them to `int` using `strconv.Atoi()`.

```go
import (
	"strconv"
	"strings"
)

func Digits(n int) []int {
	s := strconv.Itoa(n)
	d := make([]int, len(s))
	for i, l := range strings.Split(s, "") {
		d[i], _ = strconv.Atoi(l)
	}
	return d
}
```

```go
Digits(123) // [1 2 3]
```
