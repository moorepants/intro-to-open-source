# Shell Command Syntax

Shell commands are structure like so:

```
$ <program> <subcommand> <flags> <arguments>
```

program: The name of the program/command you are calling, e.g. `git` or `pwd`.

subcommand: Some shell commands have a sub command, which is optional. Git has
lots of subcommands, e.g. in `git init` `init` is the subcommand.

flags: Flags are optional and are denoted by their short version that starts
with a single dash, e.g. `-h`, or their long version, e.g. `--help`. These help
you set options or do different things. Some flags take their own arguments,
e.g. `--output-file=my_file.txt` or `--output-file my_file.txt`.

arguments: This is require option. So if you want to list all contents in the
`data/` directory, then you will use `ls data/` where `ls` is the command and
`data/` is the main argument. Arguments are often files or directories.

To get some help for a command you can open its manual (press q to get out of
the manual):

```
$ man ls
```

or use the help flag:

```
$ git init -h
```

# Some useful commands:

"working directory" is the current directory you are located in. To show the
full (p)ath to the (w)orking (d)irectory:

```
$ pwd
```

To list the files in the working directory:

```
$ ls
```

List all of the files including hidden files (those that start with a `.`) in
the working directory:

```
$ ls -a
```

Make a new directory in the working directory:

```
$ mkdir <a new name of a directory>
```

Change into a directory:

```
$ cd <name of a directory in this directory>
```

Change into the parent directory:

```
$ cd ..
```

# More info

Check out Software Carpentry's shell tutorial:

http://software-carpentry.org/v5/novice/shell/index.html
