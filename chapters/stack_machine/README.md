# Stack Machine ([Postfix Notation Guide](../../README.md))

by [Charles Iliya Krempeaux](http://changelog.ca/)

---

## Prerequisite

Before you do this chapter you will need to complete the [Stack Guide](https://github.com/reiver/guide-stack).

This chapter uses the `lifo.Stack` type you create in the that **guide**.

## What

A **stack machine** is a type of **computer processor**.

A **computer processor** could be implemented in hardware, such as with an integrated-circuit microchip.
Or a **computer processor** could be implemented in software, such as part of a virtual machine.

In this **guide** we will be implementing a **stack machine** in **software** as part of a **virtual machine**.

## Type

You will create a **stack machine** by creating the following type.

```go

import (
	"io"
)

type Processor struct {
	stack lifo.Stack[int64]
	out io.Writer
}
```

In follow chapters in this **guide** you will add methods to this type to provide functionality.
