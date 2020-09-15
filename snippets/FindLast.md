---
title: FindLast
tags: collection,error,intermediate
---

Returns the value of the last element in the provided collection that satisfies the provided testing function.

- Implement an appropriate function for each type.
- Use a `for` loop to iterate over elements in the given collection, using `f` to determine if the element matches.
- Return the value of the last matching element and `nil` if a value is found.
- Use `fmt.Errorf()` to generate an appropriate error and return it alongsie a zero value for the type.

```go
import "fmt"

func FindLastInt(arr []int, f func(int) bool) (int, error) {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return arr[i], nil
		}
	}
	return 0, fmt.Errorf("No matches found")
}
func FindLastFloat64(arr []float64, f func(float64) bool) (float64, error) {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return arr[i], nil
		}
	}
	return 0.0, fmt.Errorf("No matches found")
}
func FindLastBool(arr []bool, f func(bool) bool) (bool, error) {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return arr[i], nil
		}
	}
	return false, fmt.Errorf("No matches found")
}
func FindLastString(arr []string, f func(string) bool) (string, error) {
	for i := len(arr) - 1; i >= 0; i-- {
		if f(arr[i]) {
			return arr[i], nil
		}
	}
	return "", fmt.Errorf("No matches found")
}
```

```go
FindLastInt([]int{1, 1, 2}, func(x int) bool { return x%2 == 0 }) // 2 nil
FindLastFloat64([]float64{4.0, 6.0}, func(x float64) bool { return x%2.0 == 1.0 }) // 0.0 "No matches found"
```
