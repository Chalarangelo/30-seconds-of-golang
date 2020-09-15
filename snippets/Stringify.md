---
title: Stringify
tags: string,beginner
---

Converts the given value to a string.

- Use `fmt.Sprintf()` with the `"%v"` format specifier to convert the given value to a string.

```go
import "fmt"

func Stringify(v interface{}) string {
	return fmt.Sprintf("%v", v)
}
```

```go
Stringify(90) // "90"
Stringify(2.0) // "2.0"
Stringify(true) // "true"
```
