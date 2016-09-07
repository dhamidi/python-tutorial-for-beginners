
Requires: [Running programs in the terminal](./running-in-terminal.md)

Requires: [Python: printing text](./py-print.md)

# Making decisions with `if`

Sometimes your program needs to do different things based on the
outcome of some calculation or some data you have received.  Python
offers you a way to do this using the a so-called `if` statement.

Here is how an `if` statement looks like in Python:

```
if 1 < 2:
    print('1 is less than 2')
else:
	print('something is really wrong')
```

Let's go through this line by line:

```
if 1 < 2:
```

Means "do the following only if 1 is less than 2".

```
    print('1 is less than 2')
```

This line is what Python does if it finds that `1` is indeed less than
`2`.  This could be just as well any other Python code.  Note that the
spaces at the beginning of the line are important: they tell Python
that this code should only be executed if the `1 < 2` holds true.

```
else:
```

This line tells Python that what follows now should only be executed if 1 is not less than 2.

```
	print('something is really wrong')
```

This is the code Python executes if 1 is not less than 2.  Again, the
leading spaces are important for Python.

## Structure of an `if` statement

Generally speaking the structure of an `if` statement is:

```
if <condition>:
    <consequent>
else:
	<alternative>
```

Here `<condition>` means "any valid Python expression", `<consequent>` and `<alternative>` mean "one or more Python expressions"`.

## Useful tests for conditions

In the example above you already saw `<` as a way to compare two
numbers.  Python offers many useful functions for comparing values:

	x == y -- True if x is equal to y
	x != y -- True if x is not equal to y
    x < y  -- True if x is less than y
	x > y  -- True if x is greater than y
	x <= y -- True if x is less than or equal to y
	x >= y -- True if x is greater than or equal to y
