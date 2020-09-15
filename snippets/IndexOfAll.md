---
title: IndexOfAll
tags: collection,reflection,intermediate
---

Returns all indexes of a given element in the collection, or `[-1]` if it is not present.

- Use `reflect.ValueOf()` to get the array or slice and the value to search for, `make()` to create an appropriate slice.
- Use a `for` loop with `Value.Len()` and `Value.Index()` to iterate over each element and compare it to the search value.
- Use `append()` to add indexes of matching elements to the resulting slice.

```go
import "reflect"

func IndexOfAll(params ...interface{}) []int {
	arr, v, r := reflect.ValueOf(params[0]),
		reflect.ValueOf(params[1]).Interface(),
		make([]int, 0)

	for i := 0; i < arr.Len(); i++ {
		if arr.Index(i).Interface() == v {
			r = append(r, i)
		}
	}
	if len(r) != 0 {
		return r
	}
	return []int{-1}
}
```

```go
IndexOfAll([]int{1, 2, 1, 3, 1, 1}, 1) // [0 2 4 5]
IndexOfAll([]int{1, 2, 1, 3, 1, 1}, 4) // [-1]
```
