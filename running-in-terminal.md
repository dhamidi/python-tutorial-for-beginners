# Running programs in the terminal

The terminal is where you can give commands to your computer in text
form.  Those commands are read by a program called the shell, which
then starts other programs to execute those commands.

Examples of using the terminal look like this:

```
$ date
Wed Sep  7 22:48:24 EEST 2016
```

The `$` at the beginning of a line just means that this is the line on
which you enter a command in your terminal.  The first word on that
line is called the **command**.  In this case, your **command** is
called `date`.

The lines after the one starting with `$` are the **output of the
command**.  The `date` command just prints the current time and date,
as shown in the second line in the example.

## Where you are

The shell keeps track of the directory (also called a "folder") in
which it was started.  You can find out which directory the shell
considers the current directory by using the `pwd` command:

```
$ pwd
/Users/dhamidi
```

## Specifying paths

Any paths to files you specify are relative to the current directory.  Let's look at an example:

```
$ pwd
/Users/dhamidi
$ ls
Desktop	Downloads	Pictures
$ ls Downloads
hello-world.py
```

Now if the current directory was `/Users` instead, the above would not work anymore:

```
$ pwd
/Users
$ ls
dhamidi
$ ls Downloads
ls: cannot access 'Downloads': No such file or directory
```

That is because the shell considers the current directory to be
`/Users` and there is no directory named `Downloads` in `/Users`.  To
list all downloads, we need pass more information to `ls`:

```
$ pwd
/Users
$ ls
dhamidi
$ ls dhamidi/Downloads
hello-world.py
```

There are a few shortcuts you can use when specifying paths:

- `..` means the parent directory, so when you are in `/Users/dhamidi` then `..` means the same as `/Users`.
- `.` means the current directory, so when you are in `/Users/dhamidi/Downloads`, then `.` means `/Users/dhamidi/Downloads`
- `~` means your so-called home directory (`/Users/dhamidi` on Mac OS X and `/home/dhamidi` on Linux)

## Running Python programs

You can run Python programs by using the `python3` command, followed
by the name of file containing your program.  In this example, the
Python program we want to run is contained in a file called
`Downloads/hello-world.py`.

```
$ ls Downloads
hello-world.py
$ python3 Downloads/hello-world.py
hello, world!
```

If you run just `python3`, you end up in an interactive environment to
try out Python commands.  You can exit it by pressing `C-d` (the
control key and the `d` key at the same time) when on an empty line:

```
$ python3
Python 3.5.1 (default, Aug  9 2016, 15:35:51)
[GCC 6.1.1 20160621 (Red Hat 6.1.1-3)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print('hello, world')
hello, world
>>>
```
