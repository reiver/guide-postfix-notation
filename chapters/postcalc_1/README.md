# Postfix Notation Calculator №1 ([Postfix Notation Guide](../../README.md))

by [Charles Iliya Krempeaux](http://changelog.ca/)

---

## Prerequisite

Before you do this chapter you will need to complete the [REPL Guide](https://github.com/reiver/guide-repl).

## What

In this chapter you are going to use the `post64` package you have been creating an create an text-based **application**.

This text-based **application** will be a simple postfix notation calculator, that works similar to the _vintage postfix notation calculator_ described in a previous chapter.

You will call it your application — `postcalc`

## Repository `postcalc`

Create a **postcalc** `git` repository for this **application**.

## Assignment

Now create a text-based **application**.

This application will be a **REPL**.

If a number is entered in the **REPL**, then your **application** will _push_ it onto the _stack_.

If a plus-sign (i.e., “+”) is entered in the **REPL**, then your **application** will try to _add_ the top 2 values on the _stack_.

If an equal-sign (i.e., “=”) is entered in the **REPL**, then your **application** will try to _display_ the top value on the _stack_.

If “/QUIT” is entered is entered in the **REPL**, then your **application** will exit.

## Example Session

An example session, using your `postcalc` application, might look like this:

When the application first starts the _stack_ is empty — `[]`

**USER input:**
```
12345
```

At this point, what is on the _stack_ is — `[12345]`

**USER input:**
```
2222
```

At this point, what is on the _stack_ is — `[12345 2222]`

(The top of the stack is on the right.)


**USER input:**
```
111
```

At this point, what is on the _stack_ is — `[12345 2222 111]`

**USER input:**
```
+
```

At this point, what is on the _stack_ is — `[12345 2333]`

Notice that the `2222` and `111` were removed from the top of the stack, and they were replaced by `2333`.

The `2333` on there is the result of `2333 = 2222 + 111`

**USER input:**
```
=
```

**APPLICATION output:**
```
2333
```

At this point, what is on the _stack_ is — `[12345]`

Notice that the `2333` was removed from the _stack_ when it was outputted by the application.

**USER input:**
```
33
```

At this point, what is on the _stack_ is — `[12345 33]`

**USER input:**
```
+
```

At this point, what is on the _stack_ is — `[12378]`

Notice that the `12345` and `33` were removed from the top of the stack, and they were replaced by `12378`.

The `12378` on there is the result of `12378 = 12345 + 33`.


**USER input:**
```
=
```

**APPLICATION output:**
```
12378
```

At this point, what is on the _stack_ is — `[]`

Notice that the `12378` was removed from the _stack_ when it was outputted by the application.

**USER input:**
```
/QUIT
```

At this point, the application exits.

## Check-List

* [ ] Did you `import` your `go-post64` repository, into your application?
* [ ] Did you make use of your `post64` package, in your application?
* [ ] Did you make use of the `post64.Processor` type?
* [ ] Did you make use of the `post64.Processor.Push()` method?
* [ ] Did you make use of the `post64.Processor.Add2()` method?
* [ ] Did you make use of the `post64.Processor.Limn()` method?
