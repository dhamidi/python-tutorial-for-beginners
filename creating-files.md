Requires: [Running programs in the terminal](./running-in-terminal.md)

# Creating files

Files can be created in several ways, depending on where you are.

## In Emacs

Type `C-x C-f` and enter a file name for Emacs.

It doesn't matter whether the file exists or not; if it doesn't exist,
Emacs will show you an empty text buffer and create the file once you
save it with `C-x C-s`.

## In the terminal

### Using `touch`

An empty file can be created by using the `touch` command.  Here is an example:

```
$ ls
a-file
$ touch another-file
$ ls
a-file     another-file
```

If the file already exists, `touch` just updates the access time on
the file.  The access time of a file tells everyone when the file was
last accessed.

### Using output redirections

When typing commands in your terminal, the output of any command can
be written to file instead of showing it to in the terminal directly.
Here is an example terminal session that illustrates this:

```
$ ls
$ date
Wed Sep  7 22:43:01 EEST 2016
$ date > now
$ ls
now
$ cat now
Wed Sep  7 22:43:03 EEST 2016
```

The first time `ls` is run in this example, no files exist.  Then
`date` is used to show us the current date.

Now `date` is used again, but we are redirecting its output to a file
using ` > now`.  This will write the output of `date` to a file called
`now`.  Running `ls` again shows us the new file.

By running `cat` we look at the contents of the file and see that the
contents are the current time, just like `date` outputs it.
