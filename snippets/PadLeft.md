---
title: PadLeft
tags: string,beginner
---

Pads the given string from the start with spaces until the resulting string reaches the given length.

- Use `fmt.Sprintf()` wih an appropriate format specifier to return the formatted value.

```go
import "fmt"

func PadLeft(s string, l int) string {
	f := "%" + strconv.Itoa(l) + "v"
	return fmt.Sprintf(f, s)
}
```

```go
PadLeft("go", 8) // "      go"
```
