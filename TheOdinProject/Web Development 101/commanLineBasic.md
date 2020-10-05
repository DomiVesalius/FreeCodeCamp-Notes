# Command Line Basics

## Conquering the Command Line Ch.1 Notes

### 1.1 Home Directory (~)
All linux systems have a home directory. On Ubuntu the directory is given as: ``/home/<username>``.

```shell
$ pwd
/Users/domi
```

Home directory is where your:
1. Settings files get stored.
2. Desktop is kept.
3. Will save documents that are yours and not to be shared with others.

### 1.2 Present Working Directory
Knowing which directory you are currently in helps you in building paths to other files and can also help if you get lost. The ``pwd`` command lets you know where you are in your computer

```shell
$ pwd
/Users/domi
```

By default, ``pwd`` lists the *logical* path of your current directory (treats symlinked paths as if they were the actual paths).

If we want to see the actual physical path with all of the symlinks resolved, just use the ``-P`` flag along with ``pwd``.

```shell
$ pwd -P
```

### 1.3 List Files and Directories
We use the ``ls`` command to be able to see what files and directories arein your current directory or another directory.

```shell
$ ls
```

Entering this command will give you a list of directories and files within your current working directory.

**Listing a Different Directory**

By default, ``ls`` operates in the current working directory. ``ls`` allows you to pass a path and will return all the files and directories within that path.

```shell
$ ls /usr/local/
```

This will return a list of all the files and directories within the ``/usr/local/`` filepath.

**Listing All Files**

``ls`` only lets you see all the *visible* files and directories listed but it's common for unix and linux based machines to have invisible/hidden files that are prefixed with a '.' (dot).

In order to see all files, including the hidden ones, we execute the following command in the shell:

```shell
$ ls -a
```

The ``-a`` lets the shell know that you want all the files within that directory.

**Long Form Listing**

We can use the ``-l`` flag that will list out the names of the files and directories as well as give more details about them:

```shell
$ ls -l
```

**Human Readable Sizes**

The ``-l`` flag let us see the number of bytes in the files within that directory but it is more useful to see this type of information in human readable terms. To do this we must use the ``-h`` flag combined with the previous ``-l`` command.

```shell
$ ls -lh
```

**Sorting by Size**

Another usefull flag we can use with ls is ``-s`` which will sort the results of ls by file size instead of name.

```shell
$ ls -lhs
```

**Sorting by Last Modified Time**

To sort ls results by the last time files were modified, we use the ``-t`` flag.

```shell
$ ls -lt
```

**Reverse Sort**

To sort ls results in reverse order we use the ``-r`` flag.

```shell
$ ls -lr
```

We can also use the ``-r`` flag with the other options to reverse their sort order.