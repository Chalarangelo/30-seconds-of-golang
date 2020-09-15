---
title: IsPalindrome
tags: string,intermediate
---

Returns `true` if the given string is a palindrome, `false` otherwise.

- Use `strings.Fields()`, `strings.Join()` and `strings.ToLower()` to get the normalized, lowercase string without spaces.
- Use `range` to iterate over the string and compare each rune to the one in the reversed string.

```go
import "strings"

func IsPalindrome(s string) bool {
	v := strings.ToLower(strings.Join(strings.Fields(s), ""))
	for i := range v {
		if v[len(v)-i-1] != v[i] {
			return false
		}
	}
	return true
}
```

```go
IsPalindrome("taco cat") // true
```
