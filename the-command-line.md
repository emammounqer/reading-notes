# The Command Line

## The Command Line - What is it, how does it work and how do I get to one ?

A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.

To get to one ,If you're on a Mac then you'll find the program Terminal under Applications -> Utilities. An easy way to get to it is the key combination 'command + space' which will bring up Spotlight, then start typing Terminal and it will soon show up.
If on Linux then you will probably find it in Applications -> System or Applications -> Utilities. Alternatively you may be able to 'right-click' on the desktop and there may be an option 'Open in terminal'.
If you are on Windows and intend to remotely log into another machine then you will need an SSH client. A rather good one is Putty (free) .

## Basic Navigation - An introduction to the Linux directory system and how to get around it ?

Print Working Directory - ie. Where are we currently.

```bash
pwd
```

List the contents of a directory.

```bash
ls
```

Change Directories - ie. move to another directory.

```bash
cd
```

## More About Files - Find out some interesting characteristics of files and directories in a Linux environment ?

- **Everything is a File**

    with linux is that under the hood, everything is actually a file

- **Linux is an Extensionless System:**

    Files can have any extension they like or none at all

- **Linux is Case Sensitive:
**
    it is possible to have two or more files and directories with the same name but letters of different case.

- **Spaces in names**

    a space on the command line is how we seperate items so if we have a file or directory with a space in its name then we need to put it in quotes or escape the space.

  - **Quotes**
  
    the first approach involves using quotes around the entire item
  - **Escape Characters**

    Another method is to use what is called an escape character, which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.

- *If the file or directory's name begins with a . (full stop) then it is considered to be hidden*

## Manual Pages - Learn how to make the most of the Linux commands you are learning ?

### The manual pages

Look up the manual page for a particular command.

```bash
man <command to look up>
```

### Searching

It is possible to do a keyword search on the Manual pages.

```bash
man -k <search term>
```

Within a manual page, perform a search for 'term'

```bash
/<term>
```

After performing a search within a manual page, select the next found item.

```bash
n
```

## File Manipulation - How to make, remove, rename, copy and move files and directories ?

### Make a directory

```bash
mkdir <directory name>
```

### Remove a directory

```bash
rmdir <directory name>
```

### Create Blank File

```bash
touch <file name>
```

### Copying Files or Directories

```bash
cp <source> <destination>
```

### moving Files or Directories

```bash
mv <source> <destination>
```

### Remove a file

```bash
rm <file name>
```

### Remove a directory and all its contents

```bash
rm -r <directory name>
```

***NOTE:***  The Linux command line does not have an undo feature. Perform destructive actions carefully.

## Cheat Sheet - A quick reference for the main points covered in this tutorial ?

[Cheat Sheet Link](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)
