---
title: Includes
tags: collection,reflection,intermediate
---

Returns `true` if the given element can be found in the collection, `false` otherwise.

- Use `reflect.ValueOf()` to get the array or slice and the value to search for.
- Use a `for` loop with `Value.Len()` and `Value.Index()` to iterate over each element and compare it to the search value.
- Return `true` if a matching value is found, `false` otherwise.

```go
import "reflect"

func Includes(params ...interface{}) bool {
	arr, v := reflect.ValueOf(params[0]),
		reflect.ValueOf(params[1]).Interface()

	for i := 0; i < arr.Len(); i++ {
		if arr.Index(i).Interface() == v {
			return true
		}
	}
	return false
}
```

```go
MySnippet() // "result"
```
