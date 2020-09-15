---
title: PadRight
tags: string,beginner
---

Pads the given string from the end with spaces until the resulting string reaches the given length.

- Use `fmt.Sprintf()` wih an appropriate format specifier to return the formatted value.

```go
import "fmt"

func PadRight(s string, l int) string {
	f := "%" + strconv.Itoa(-l) + "v"
	return fmt.Sprintf(f, s)
}
```

```go
PadRight("go", 8) // "go      "
```
