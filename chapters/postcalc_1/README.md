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

If “/DIE” is entered is entered in the **REPL**, then your **application** will exit.

An example session might look like this:

USER:
```
12345
```

(At this point, what is on the _stack_ is `[12345]`)

USER:
```
2222
```

(At this point, what is on the _stack_ is `[12345 2222]`)


USER:
```
111
```

(At this point, what is on the _stack_ is `[12345 2222 111]`)

USER:
```
+
```

(At this point, what is on the _stack_ is `[12345 2333]`)

USER:
```
=
```

APPLICATION:
```
2333
```

(At this point, what is on the _stack_ is `[12345]`)

USER:
```
33
```

(At this point, what is on the _stack_ is `[12345 33]`)

USER:
```
+
```

(At this point, what is on the _stack_ is `[12378]`)


USER:
```
=
```

APPLICATION:
```
12378
```

(At this point, what is on the _stack_ is `[]`)

USER:
```
/DIE
```

(At this point, the application exits.)