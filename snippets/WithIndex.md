---
title: WithIndex
tags: collection,map,reflection,intermediate
---

Returns a map with index-value pairs.

- Use `reflect.ValueOf()` to get the array or slice, `make()` to create a new `map`.
- Use a `for` loop with `Value.Len()`, `Value.Index()` and `Value.Interface()` to iterate over each element and add it to the map.

```go
import "reflect"

func WithIndex(params ...interface{}) map[int]interface{} {
	arr, m := reflect.ValueOf(params[0]),
		make(map[int]interface{})
	for i := 0; i < arr.Len(); i++ {
		m[i] = arr.Index(i).Interface()
	}
	return m
}
```

```go
WithIndex([]int{4, 3, 2, 1}) // [0:4 1:3 2:2 3:1]
```
