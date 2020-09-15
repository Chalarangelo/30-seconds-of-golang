---
title: Dedupe
tags: collection,map,intermediate
---

Deduplicates the elements in a given array or slice.

- Implement an appropriate function for each type.
- Use `make()` to create a `map` and an appropriate slice.
- Use `range` to iterate over the elements in the collection and the map to check if they have been seen before.
- Use `append()` to add unique values to the slice.

```go
func DedupeInts(arr []int) []int {
	m, uniq := make(map[int]bool), make([]int, 0)
	for _, v := range arr {
		if _, ok := m[v]; !ok {
			m[v], uniq = true, append(uniq, v)
		}
	}
	return uniq
}
func DedupeFloat64s(arr []float64) []float64 {
	m, uniq := make(map[float64]bool), make([]float64, 0)
	for _, v := range arr {
		if _, ok := m[v]; !ok {
			m[v], uniq = true, append(uniq, v)
		}
	}
	return uniq
}
func DedupeStrings(arr []string) []string {
	m, uniq := make(map[string]bool), make([]string, 0)
	for _, v := range arr {
		if _, ok := m[v]; !ok {
			m[v], uniq = true, append(uniq, v)
		}
	}
	return uniq
}
```

```go
DedupeInts([]int{1, 2, 1, 2, 3, 3, 4}) // [1 2 3 4]
```
