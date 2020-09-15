---
title: IndexOf
tags: collection,reflection,intermediate
---

Returns the first index at which a given element can be found in the collection, or `-1` if it is not present.

- Use `reflect.ValueOf()` to get the array or slice and the value to search for.
- Use a `for` loop with `Value.Len()` and `Value.Index()` to iterate over each element and compare it to the search value.
- Return the index if a matching value is found, `-1` otherwise.

```go
import "reflect"

func IndexOf(params ...interface{}) int {
	arr, v := reflect.ValueOf(params[0]),
		reflect.ValueOf(params[1]).Interface()

	for i := 0; i < arr.Len(); i++ {
		if arr.Index(i).Interface() == v {
			return i
		}
	}
	return -1
}
```

```go
IndexOf([]int{1, 2, 3}, 2) // 1
IndexOf([]int{1, 2, 3}, 4) // -1
```
