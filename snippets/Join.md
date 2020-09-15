---
title: Join
tags: collection,string,reflection,intermediate
---

Returns a string by concatenating all of the elements in the collection, separated by the specified separator string.

- Use `reflect.ValueOf()` to get the array or slice and the separator string, `make()` to create an appropriate string slice.
- Use a `for` loop with `Value.Len()` and `Value.Index()` to iterate over each element, `fmt.Sprintf()` to convert it to a string.
- Use `strings.Join()` to combine the strings using the separator provided.

```go
import (
	"fmt"
	"reflect"
	"strings"
)

func Join(params ...interface{}) string {
	arr, sp := reflect.ValueOf(params[0]),
		reflect.ValueOf(params[1]).String()
	ars := make([]string, arr.Len())

	for i := 0; i < arr.Len(); i++ {
		ars[i] = fmt.Sprintf("%v", arr.Index(i))
	}

	return strings.Join(ars, sp)

}
```

```go
Join([]int{1, 2, 3}, ".") // "1.2.3"
```
