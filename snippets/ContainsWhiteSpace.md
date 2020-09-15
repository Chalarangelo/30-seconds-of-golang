---
title: ContainsWhiteSpace
tags: string,regexp,beginner
---

Returns a string with whitespaces compacted.

- Use `Regexp.MatchString()` with a regular expression to check if the given string contains any whitespace characters.

```go
import "regexp"

func ContainsWhiteSpace(str string) bool {
	re := regexp.MustCompile(`\s`)
	return re.MatchString(str)
}
```

```go
ContainsWhiteSpace("lorem") // false
ContainsWhiteSpace("lorem ipsum") // true
```
