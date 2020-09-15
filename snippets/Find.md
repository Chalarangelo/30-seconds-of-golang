---
title: Find
tags: collection,error,intermediate
---

Returns the value of the first element in the provided collection that satisfies the provided testing function.

- Implement an appropriate function for each type.
- Use `range` to iterate over elements in the given collection, using `f` to determine if the element matches.
- Return the value of the first matching element and `nil` if a value is found.
- Use `fmt.Errorf()` to generate an appropriate error and return it alongsie a zero value for the type.

```go
import "fmt"

func FindInt(arr []int, f func(int) bool) (int, error) {
	for _, v := range arr {
		if f(v) {
			return v, nil
		}
	}
	return 0, fmt.Errorf("No matches found")
}
func FindFloat64(arr []float64, f func(float64) bool) (float64, error) {
	for _, v := range arr {
		if f(v) {
			return v, nil
		}
	}
	return 0.0, fmt.Errorf("No matches found")
}
func FindBool(arr []bool, f func(bool) bool) (bool, error) {
	for _, v := range arr {
		if f(v) {
			return v, nil
		}
	}
	return false, fmt.Errorf("No matches found")
}
func FindString(arr []string, f func(string) bool) (string, error) {
	for _, v := range arr {
		if f(v) {
			return v, nil
		}
	}
	return "", fmt.Errorf("No matches found")
}
```

```go
FindInt([]int{1, 1, 2}, func(x int) bool { return x%2 == 0 }) // 2 nil
FindFloat64([]float64{4.0, 6.0}, func(x float64) bool { return x%2.0 == 1.0 }) // 0.0 "No matches found"
```
