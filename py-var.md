Requires: [Running programs in the terminal](./running-in-terminal.md)
Requires: [Python: printing text](./py-print.md)

# Variables

Variables are names for values in Python.  By giving a name to a
value, you can later refer to that value without having to spell it
out every time.

## Creating variables


Variables are created once you *assign a value* to them.  In Python
code *assigning a value to a variable* looks like this:

```
income_tax_rate = 0.2
```

Here we *assign the value* `0.2` to a variable named `income_tax_rate`

## Using variables

To use a variable in an expression, you just write its name where you
want to use it.  For example, to calculate the income tax somebody
needs to pay for a service worth 50 EUR, we can use the following
Python code:

```
price = 50
income_tax_rate = 0.2
print(price * income_tax)
```

This has the same effect as writing:

```
print(50 * 0.2)
```

However, by using variables it is easier to understand what the
program is doing, because those numbers (`50` and `0.2` in the
example) have useful names (`price` and `income_tax_rate`).
