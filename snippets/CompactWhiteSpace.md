---
title: CompactWhiteSpace
tags: string,regexp,beginner
---

Returns a string with whitespaces compacted.

- Use `Regexp.ReplaceAllString()` with a regular expression to replace all occurrences of 2 or more whitespace characters with a single space.

```go
import "regexp"

func CompactWhiteSpace(str string) string {
	re := regexp.MustCompile(`\s{2,}`)
	return re.ReplaceAllString(str, " ")
}
```

```go
CompactWhiteSpace("Lorem    Ipsum") // "Lorem Ipsum"
CompactWhiteSpace("Lorem \n Ipsum") // "Lorem Ipsum"
```
