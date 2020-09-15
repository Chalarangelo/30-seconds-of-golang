---
title: Filter
tags: collection,intermediate
---

Returns a new slice with all elements that pass the test implemented by the provided function.

- Implement an appropriate function for each type.
- Use `make()` to create an appropriate slice.
- Use `range` to iterate over elements in the given collection, using `append()` to add them to the resulting slice based on the result of `fn`.
- The functions can be tweaked to allow for an index to be passed to `fn` as a second argument, if desired.

```go
func FilterInt(arr []int, f func(int) bool) []int {
	arf := make([]int, 0)
	for _, v := range arr {
		if f(v) {
			arf = append(arf, v)
		}
	}
	return arf
}
func FilterFloat64(arr []float64, f func(float64) bool) []float64 {
	arf := make([]float64, 0)
	for _, v := range arr {
		if f(v) {
			arf = append(arf, v)
		}
	}
	return arf
}
func FilterBool(arr []bool, f func(bool) bool) []bool {
	arf := make([]bool, 0)
	for _, v := range arr {
		if f(v) {
			arf = append(arf, v)
		}
	}
	return arf
}
func FilterString(arr []string, f func(string) bool) []string {
	arf := make([]string, 0)
	for _, v := range arr {
		if f(v) {
			arf = append(arf, v)
		}
	}
	return arf
}
```

```go
intCheck := func(x int) bool { return x > 1 }
FilterInt([]int{0, 2}, intCheck) // [2]
float64Check := func(x float64) bool { return x > 0.5 }
FilterFloat64([]float64{0.0, 1.0}, float64Check) // [1.0]
boolCheck := func(x bool) bool { return x }
FilterBool([]bool{false, true}, boolCheck) // [true]
stringCheck := func(x string) bool { return len(x) > 1 }
FilterString([]string{"", "hi"}, stringCheck) // ["hi"]
```
