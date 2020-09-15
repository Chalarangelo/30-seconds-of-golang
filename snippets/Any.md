---
title: Any
tags: collection,intermediate
---

Returns `true` if at least one element in the collection passes the test implemented by the provided function, `false` otherwise.

- Implement an appropriate function for each type.
- Use `range` to iterate over elements in the given collection, returning `true` or `false` based on the result of `fn`.
- The functions can be tweaked to allow for an index to be passed to `fn` as a second argument, if desired.

```go
func AnyInt(arr []int, fn func(int) bool) bool {
	for _, v := range arr {
		if fn(v) {
			return true
		}
	}
	return false
}
func AnyFloat64(arr []float64, fn func(float64) bool) bool {
	for _, v := range arr {
		if fn(v) {
			return true
		}
	}
	return false
}
func AnyBool(arr []bool, fn func(bool) bool) bool {
	for _, v := range arr {
		if fn(v) {
			return true
		}
	}
	return false
}
func AnyString(arr []string, fn func(string) bool) bool {
	for _, v := range arr {
		if fn(v) {
			return true
		}
	}
	return false
}
```

```go
intCheck := func(x int) bool { return x > 1 }
AnyInt([]int{0, 2}, intCheck) // true
float64Check := func(x float64) bool { return x > 0.5 }
AnyFloat64([]float64{0.0, 1.0}, float64Check) // true
boolCheck := func(x bool) bool { return x }
AnyBool([]bool{false, true}, boolCheck) // true
stringCheck := func(x string) bool { return len(x) > 1 }
AnyString([]string{"", "hi"}, stringCheck) // true
```
