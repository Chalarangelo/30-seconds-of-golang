---
title: FindLastIndex
tags: collection,beginner
---

Returns the index of the last element in the provided collection that satisfies the provided testing function, `-1` otherwise.

- Implement an appropriate function for each type.
- Use a `for` loop to iterate over elements in the given collection, using `f` to determine if the element matches.
- Return the index of the last matching element or `-1` if none is found.

```go
func FindLastIndexInt(arr []int, f func(int) bool) int {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return i
		}
	}
	return -1
}
func FindLastIndexFloat64(arr []float64, f func(float64) bool) int {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return i
		}
	}
	return -1
}
func FindLastIndexBool(arr []bool, f func(bool) bool) int {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return i
		}
	}
	return -1
}
func FindLastIndexString(arr []string, f func(string) bool) int {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return i
		}
	}
	return -1
}
```

```go
FindLastIndexInt([]int{1, 1, 2}, func(x int) bool { return x%2 == 0 }) // 2
FindLastIndexFloat64([]float64{4.0, 6.0}, func(x float64) bool { return x%2.0 == 1.0 }) // -1
```
