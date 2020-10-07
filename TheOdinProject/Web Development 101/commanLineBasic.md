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

### 1.4 Links
Links allow us to create an association from one file/directory to another. This is useful for maintaining a file system or having multiple versions of a file or directory, and not wanting to use disk space to store copies of those files.

Links can be 'symbolic' or 'hard'.

**Hard LInks**

The ``ln`` command is used to create a linke between two files and by default, it will be a hard link.
- Hard links create an identical copy of the linked file on disk which will get updated automatically as the source file gets updated.

The following is the syntax of creating such a link:

```shell
$ ln <source_file>.<type> <target_file>.<type>
```

So if we wanted to hard link two files named a.txt and b.txt with a.txt being the source file it would go as:

```shell
$ ln a.txt b.txt
```

Note that hard links only work on the current file system and you cannot create a hard link to a file on a different system.

If the source file gets deleted, the target file wil lcontinue to live as an independent file.

**Forcing a Link**

When the source file you are trying to link already exists you will get an error. In order to bypass this error we have to force a link using the ``-f`` flag.

```shell
$ ln -f a.txt b.txt
```

**Symbolic Links**

We use these when we want to link directories but they can also be used for linking to files.

Symbolic links can also link to files or directories on other file systems. To create a symbolic link we use the ``-s`` flag.

```shell
$ ln -s a.txt b.txt
```

### Change Directories
We use the ``cd`` command to change directories. It takes one argument which is the path to the directory you want to navigate to.

```shell
$ cd ~/Documents
```

**Navigating Up**

Sometimes when we are in a directory we want to go to the previous directory (move up to a parent directory). Instead of providing the whole path, we can use the special path ``..``

```shell
$ cd ..
```

**Navigating to Home Directory**

When you want to navigate to your home directory you must call ``cd`` without any arguments.

```shell
$ cd
$ pwd
$ /Users/domi
```

### 1.6 Creating Directories
To create a directory we use the ``mkdir`` command followed by the name of the directory we wish to create.

```shell
$ mkdir foo
```

**Create Intermediate Directories**

The ``mkdir`` command allows us to create nested directories using the ``-p`` flag.

```shell
$ mkdir -p a/b/c
```

**Verbose Output**

Adding the ``-v`` flag will print the results of the ``mkdir`` to the console:

```shell
$ mkdir -v a
mkdir: created directory 'a'
```