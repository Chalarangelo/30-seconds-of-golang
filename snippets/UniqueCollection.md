---
title: UniqueCollection
tags: collection, map
---

Returns the unique collection of each type from given collection

- Implemented unique function for string, int and float64 types.
- Use `keys` map variable to store the value from given slice.
- Use `list` to store the unique elements.
- Use `for` loop to iterate the given slice.
- If element is absent in `keys` map, then it will append it `list` otherwise continue to next iteration.
- Try to explain everything briefly but clearly.

```go
func UniqueStringCollection(slice []string) (list []string) {
	 keys := make(map[string]bool)
	 for _, entry := range slice{
	 	if _, ok := keys[entry]; !ok{
	 		keys[entry] = true
	 		list = append(list, entry)
		}
	 }
	 return
}

func UniqueIntCollection(slice []int) (list []int) {
	 keys := make(map[int]bool)
	 for _, entry := range slice{
	 	if _, ok := keys[entry]; !ok{
	 		keys[entry] = true
	 		list = append(list, entry)
		}
	 }
	 return
}

func UniqueFloat64Collection(slice []float64) (list []float64) {
	 keys := make(map[float64]bool)
	 for _, entry := range slice{
	 	if _, ok := keys[entry]; !ok{
	 		keys[entry] = true
	 		list = append(list, entry)
		}
	 }
	 return
}

```

```go
UniqueStringCollection([]string{"1", "3", "5", "3"}) // ["1", "3", "5"]
UniqueIntCollection([]int{1, 3, 5, 3}) // [1, 3, 5]
UniqueFloat64Collection([]float64{1.47, 3.65, 4.81, 3.65, 3.32}) // [1.47, 3.65, 4.81, 3.32]
```
