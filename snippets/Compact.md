---
title: Compact
tags: collection,reflection,intermediate
---

Removes zero values from a collection.

- Use `reflect.ValueOf()` to get the array or slice, `make()` to make an appropriate slice.
- Use a `for` loop with `Value.Len()` and `Value.Index()` to iterate over each element.
- Use `append()` to add it to the resulting slice if `Value.IsZero()` is `false.

```go
import "reflect"

func Compact(params ...interface{}) []reflect.Value {
	arr := reflect.ValueOf(params[0])
	r := make([]reflect.Value, 0)

	for i := 0; i < arr.Len(); i++ {
		if !arr.Index(i).IsZero() {
			r = append(r, arr.Index(i))
		}
	}
	return r
}
```

```go
arr := []float64{1, 0, 5, 2}
arc := make([]float64, 0)
for _, v := range Compact(arr) {
  arc = append(arc, v.Float())
}
// arc = [1 5 2]
```
