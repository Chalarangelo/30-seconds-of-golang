---
title: Mask
tags: string,beginner
---

Replaces all but the last `n` of characters with the specified mask character.

- Slice the given string appropriately, using `strings.Repeat()` to add `n` times `m` to the beginning.

```go
import "strings"

func Mask(cc string, n int, m rune) string {
	return strings.Repeat(string(m), len(cc)-n) + cc[len(cc)-n:]
}
```

```go
Mask("1234567890", 4, '*') // "******7890"
```
