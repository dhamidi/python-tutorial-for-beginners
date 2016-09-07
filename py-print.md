Requires: [Running programs in the terminal](./running-in-terminal.md)

# Printing output to the user

You can show text to the user using the `print` function in Python.
You write it like this:

```
print('hello, world!')
```

This line *calls the function* `print` and stuff between the
parentheses (`(` and `)`) is called "arguments" by programmers.  In this case, the `print` function is called with one *argument*, the string `hello, world!`.

## Trying this code out

You can try this code out in two ways:

1. Write it into a new file (e.g. `hello-world.py`) and run it from the terminal: `python3 hello-world.py`

2. Start the interactive Python interpreter by running `python3` in your terminal, enter `print('hello, world!')` and then press the `Return` key.  You should see something like this:

   ```
   Python 3.5.1 (default, Aug  9 2016, 15:35:51)
   [GCC 6.1.1 20160621 (Red Hat 6.1.1-3)] on linux
   Type "help", "copyright", "credits" or "license" for more information.
   >>> print('hello, world!')
   hello, world!
   >>>
   ```

## Strings

If `print` is a function, how can we write a Python program that shows
the word "print"?  Let's see what happens if we just try naively the
first thing that comes to mind:

```
$ python3
Python 3.5.1 (default, Aug  9 2016, 15:35:51)
[GCC 6.1.1 20160621 (Red Hat 6.1.1-3)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(print)
<built-in function print>
```

Fair enough, Python tells us that `print` refers to a function built
into Python and that this function is called `print`.

To tell Python that you mean the literal text, as you have written it,
you need to put single quotes (`'`) around the text:

```
$ python3
Python 3.5.1 (default, Aug  9 2016, 15:35:51)
[GCC 6.1.1 20160621 (Red Hat 6.1.1-3)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('print')
print
```

A bit of text enclosed by single quotes is called a **string**.
Python leaves strings alone and doesn't try to interpret their meaning
in any way.

When writing strings in your program, note that **strings cannot contain line breaks:**

```
>>> print('first line
  File "<stdin>", line 1
    print('first line
                    ^
SyntaxError: EOL while scanning string literal
```

`SyntaxError` means that what we have written cannot be recognized by
Python, i.e. we have made a spelling mistake or mistyped something and
`EOL` is short for `End of line`.  What Python is telling us is:

> I tried to read a string literal, but before I reached the end of
> the string literal, I reached the end of the line.  I don't know
> what to do with this!

Luckily Python has a solution for this.  If you need line breaks in
your strings, you can use three single quotes in a row for delimiting
your string:

```
>>> print('''first line
... second line
... third line
... ''')
first line
second line
third line

>>>
```
