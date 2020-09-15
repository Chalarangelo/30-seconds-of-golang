---
title: AllSame
tags: collection,reflection,intermediate
---

Returns `true` if all elements in the collection have the same value, `false` otherwise.

- Use `reflect.ValueOf()` to get the array or slice, `Value.Index()` and `Value.Interface()` to get the first value.
- Use a `for` loop with `Value.Len()` and `Value.Index()` to iterate over each element and compare it to the search value.
- Return `false` if a non-matching value is found, `true` otherwise.

```go
import "reflect"

func AllSame(params ...interface{}) bool {
	arr := reflect.ValueOf(params[0])
	v := arr.Index(0).Interface()

	for i := 0; i < arr.Len(); i++ {
		if arr.Index(i).Interface() != v {
			return false
		}
	}
	return true
}
```

```go
AllSame([]int{1, 2, 3, 4, 5, 6}) // false
AllSame([]int{1, 1, 1, 1}) // true
```
