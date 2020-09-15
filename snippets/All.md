---
title: All
tags: collection,intermediate
---

Returns `true` if all elements in the collection pass the test implemented by the provided function, `false` otherwise.

- Implement an appropriate function for each type.
- Use `range` to iterate over elements in the given collection, returning `true` or `false` based on the result of `fn`.
- The functions can be tweaked to allow for an index to be passed to `fn` as a second argument, if desired.

```go
func AllInt(arr []int, fn func(int) bool) bool {
	for _, v := range arr {
		if !fn(v) {
			return false
		}
	}
	return true
}
func AllFloat64(arr []float64, fn func(float64) bool) bool {
	for _, v := range arr {
		if !fn(v) {
			return false
		}
	}
	return true
}
func AllBool(arr []bool, fn func(bool) bool) bool {
	for _, v := range arr {
		if !fn(v) {
			return false
		}
	}
	return true
}
func AllString(arr []string, fn func(string) bool) bool {
	for _, v := range arr {
		if !fn(v) {
			return false
		}
	}
	return true
}
```

```go
intCheck := func(x int) bool { return x > 1 }
AllInt([]int{4, 2}, intCheck) // true
float64Check := func(x float64) bool { return x > 0.5 }
AllFloat64([]float64{0.8, 1.0}, float64Check) // true
boolCheck := func(x bool) bool { return x }
AllBool([]bool{true, true}, boolCheck) // true
stringCheck := func(x string) bool { return len(x) > 1 }
AllString([]string{"go", "hi"}, stringCheck) // true
```
