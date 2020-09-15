---
title: Zip
tags: collection,reflection,advanced
---

Creates a collection of elements, grouped based on the position in the original collections.

- Use `range` to iterate over the `params`, `reflect.ValueOf()` and `Value.Len()` to find the longest collection.
- Use `make()` to create a 2D `interface{}` slice of length equal to the longest collection.
- Use `make()` to create a slice for each element in the result, `range` to iterate over `params`.
- Use `reflect.ValueOf()`, `Value.Len()`, `append()`, `Value.Index()` and `Value.Interface()` to add values to the result.

```go
import "reflect"

func Zip(params ...interface{}) [][]interface{} {
	l := 0
	for i := range params {
		arr := reflect.ValueOf(params[i])
		if l < arr.Len() {
			l = arr.Len()
		}
	}
	r := make([][]interface{}, l)

	for i := 0; i < l; i++ {
		r[i] = make([]interface{}, 0)
		for j := range params {
			v := reflect.ValueOf(params[j])
			if v.Len() > i {
				r[i] = append(r[i], v.Index(i).Interface())
			}
		}
	}
	return r
}
```

```go
s := []string{"a", "b"}
i := []int{1, 2}
b := []bool{true, false}
Zip(s, i, b) // [[a 1 true] [b 2 false]]
```
