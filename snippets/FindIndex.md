---
title: FindIndex
tags: collection,beginner
---

Returns the index of the first element in the provided collection that satisfies the provided testing function, `-1` otherwise.

- Implement an appropriate function for each type.
- Use `range` to iterate over elements in the given collection, using `f` to determine if the element matches.
- Return the index of the first matching element or `-1` if none is found.

```go
func FindIndexInt(arr []int, f func(int) bool) int {
	for i, v := range arr {
		if f(v) {
			return i
		}
	}
	return -1
}
func FindIndexFloat64(arr []float64, f func(float64) bool) int {
	for i, v := range arr {
		if f(v) {
			return i
		}
	}
	return -1
}
func FindIndexBool(arr []bool, f func(bool) bool) int {
	for i, v := range arr {
		if f(v) {
			return i
		}
	}
	return -1
}
func FindIndexString(arr []string, f func(string) bool) int {
	for i, v := range arr {
		if f(v) {
			return i
		}
	}
	return -1
}
```

```go
FindIndexInt([]int{1, 1, 2}, func(x int) bool { return x%2 == 0 }) // 2
FindIndexFloat64([]float64{4.0, 6.0}, func(x float64) bool { return x%2.0 == 1.0 }) // -1
```
