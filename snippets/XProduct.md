---
title: XProduct
tags: collection,reflection,intermediate
---

Creates a new slice out of the two supplied by creating each possible pair from the collections.

- Use `reflect.ValueOf()` to get the arrays or slices, `Value.Len()` and `make()` to create an appropriate slice for the result.
- Use a `for` loop with `Value.Len()`, `Value.Index()` and `Value.Interface()` to populate the result.

```go
import "reflect"

func XProduct(params ...interface{}) [][]interface{} {
	a, b := reflect.ValueOf(params[0]), reflect.ValueOf(params[1])
	l := a.Len() * b.Len()
	r := make([][]interface{}, l)

	for i := 0; i < l; i++ {
		r[i] = []interface{}{
			a.Index(i % a.Len()).Interface(),
			b.Index((i / a.Len()) % b.Len()).Interface(),
		}
	}
	return r

}
```

```go
XProduct([]int{1, 2}, []string{"a", "b"}) // [[1 a] [2 a] [1 b] [2 b]]
```
