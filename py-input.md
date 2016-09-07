Requires: [Running programs in the terminal](./running-in-terminal.md)
Requires: [Python: variables](./py-var.md)
Requires: [Python: printing text](./py-print.md)

# Getting data from the user

Python allows you to ask the user for text when running in a terminal.
You can do so by using the `input` function Python provides.  Here is
an example of using the input function in the interactive Python
interpreter:

```
$ python3
Python 3.5.1 (default, Aug  9 2016, 15:35:51)
[GCC 6.1.1 20160621 (Red Hat 6.1.1-3)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> input('What is your name: ')
What is your name: John Doe
'John Doe'
>>>
```

When Python sees `input('What is your name: ')` it shows the first
argument to the `input` function to the user (`'What is your name: '`)
and then waits for the user to write an answer and press the `Return`
key.

The `input` function returns the text it read from the user.  This
return value can be used in any other Python expression:

```
$ python3
Python 3.5.1 (default, Aug  9 2016, 15:35:51)
[GCC 6.1.1 20160621 (Red Hat 6.1.1-3)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('hello, " + input('What is your name: ')
What is your name: John Doe
hello, John Doe
>>>
```

Note that `+` not only adds number but also takes two strings and
glues them together:

```
>>> 'a'
'a'
>>> 'b'
'b'
>>> 'a' + 'b'
'ab'
```
