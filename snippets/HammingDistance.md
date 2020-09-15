---
title: HammingDistance
tags: math,intermediate
---

Calculates the Hamming distance between two values.

- Use the XOR operator (`^`) to find the bit difference between the two numbersand convert to a binary string using `fmt.Sprintf()` with `"%b`.
- Count and return the number of `1`s in the string, using `strings.Count()`.

```go
import (
	"fmt"
	"strings"
)

func ΗammingDistance(n, m int) int {
	return strings.Count(fmt.Sprintf("%b", n^m), "1")
}
```

```go
ΗammingDistance(2, 3) // 1
```
