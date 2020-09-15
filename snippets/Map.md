---
title: Map
tags: collection,intermediate
---

Returns a new slice populated with the results of calling the provided function on every element in the collection.

- Implement an appropriate function for each type conversion.
- Use `make()` to create an appropriate slice.
- Use `range` to iterate over elements in the given collection, setting the value at the same index in the resulting slice based on the result of `fn`.
- The functions can be tweaked to allow for an index to be passed to `fn` as a second argument, if desired.

```go
func MapInt(arr []int, fn func(int) int) []int {
	arm := make([]int, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapIntFloat64(arr []int, fn func(int) float64) []float64 {
	arm := make([]float64, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapIntBool(arr []int, fn func(int) bool) []bool {
	arm := make([]bool, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapIntString(arr []int, fn func(int) string) []string {
	arm := make([]string, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}

func MapFloat64(arr []float64, fn func(float64) float64) []float64 {
	arm := make([]float64, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapFloat64Int(arr []float64, fn func(float64) int) []int {
	arm := make([]int, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapFloat64Bool(arr []float64, fn func(float64) bool) []bool {
	arm := make([]bool, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapFloat64String(arr []float64, fn func(float64) string) []string {
	arm := make([]string, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}

func MapBool(arr []bool, fn func(bool) bool) []bool {
	arm := make([]bool, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapBoolInt(arr []bool, fn func(bool) int) []int {
	arm := make([]int, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapBoolFloat64(arr []bool, fn func(bool) float64) []float64 {
	arm := make([]float64, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapBoolString(arr []bool, fn func(bool) string) []string {
	arm := make([]string, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}

func MapString(arr []string, fn func(string) string) []string {
	arm := make([]string, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapStringInt(arr []string, fn func(string) int) []int {
	arm := make([]int, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapStringFloat64(arr []string, fn func(string) float64) []float64 {
	arm := make([]float64, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
func MapStringBool(arr []string, fn func(string) bool) []bool {
	arm := make([]bool, len(arr))
	for i, v := range arr { arm[i] = fn(v) }
	return arm
}
```

```go
import "fmt"

ints := []int{1, 2, 3}
addTwo := func(x int) int { return x + 2 }
dollarString := func(x int) string { return fmt.Sprintf("$%d", x) }
MapInt(ints, addTwo) // [3 4 5]
MapIntString(ints, dollarString) // ["$1" "$2" "$3"]

floats := []float64{3.0, 2.0, 0.0}
gtTwo := func(x float64) bool { return x > 2.0 }
MapFloat64Bool(floats, gtTwo) // [true false false]

strings := []string{"go", "is", "cool"}
strLen := func(x string) int { return len(x) }
MapStringInt(strings, strLen) // [2 2 4]
```
