---
title: Frequencies
tags: collection,map,intermediate
---

Returns a map with the unique values of the collection as keys and their frequencies as the values.

- Implement an appropriate function for each type.
- Use `make()` to create a `map`.
- Use `range` to iterate over the elements in the collection, adding to existing keys every time the same value is encountered.

```go
func FrequenciesInt(arr []int) map[int]int {
	m := make(map[int]int)
	for _, v := range arr {
		if f, ok := m[v]; ok {
			m[v] = f + 1
		} else {
			m[v] = 1
		}
	}
	return m
}
func FrequenciesFloat64(arr []float64) map[float64]int {
	m := make(map[float64]int)
	for _, v := range arr {
		if f, ok := m[v]; ok {
			m[v] = f + 1
		} else {
			m[v] = 1
		}
	}
	return m
}
func FrequenciesBool(arr []bool) map[bool]int {
	m := make(map[bool]int)
	for _, v := range arr {
		if f, ok := m[v]; ok {
			m[v] = f + 1
		} else {
			m[v] = 1
		}
	}
	return m
}
func FrequenciesString(arr []string) map[string]int {
	m := make(map[string]int)
	for _, v := range arr {
		if f, ok := m[v]; ok {
			m[v] = f + 1
		} else {
			m[v] = 1
		}
	}
	return m
}
```

```go
MySnippet() // "result"
```
