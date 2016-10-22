## A Brief History Lesson

> A Unix "shell" is a command-line interpreter that provides a traditional user interface for the Unix operating system and for Unix-like systems.

* There are a [bunch of different shells](http://www.ibm.com/developerworks/library/l-linux-shells/figure1.gif)... Bourne shell, C shell, Korn shell, Z shell, etc.
* The first major shell was the Bourne Shell, developed in the late 70's.
* We're going to focus on the "Bourne again shell" or _Bash_ (default shell for OSX and Linux)

_Hint: You can install Bash bindings in Windows via [Git for Windows](https://git-for-windows.github.io/)_

![](./images/bash.png)

---

## Why Bash?

* A fully-capable scripting language
* Vast adoption (approximately [70% of public servers](https://en.wikipedia.org/wiki/Usage_share_of_operating_systems#Public_servers_on_the_Internet) are Unix or Unix-like)
* Tons of command line features...
    * Tab completion
    * Pipes
    * Aliases
    * Environment variables
    * Startup scripts
    * ...and more!

---

## Essential Commands

In this next part, we'll learn some basic commands that we can use to interact with our Bash shell.

The outline below is provided as a handy reference of the commands we'll cover in class. [This tutorial](http://programminghistorian.org/lessons/intro-to-bash) contains alot of additional information if you're confused or just curious.
&nbsp;  

---

### Navigation

`pwd` - Display your _"present working directory"_.

`ls` - Display the contents of a directory specified by `<path>`.
> __Optional Flags:__  
> Long listing (with details)... `ls -l`  
> List all files... `ls -a`

> __Optional Arguments:__  
> Apply to files or directories... `ls <path>`

> __Hint:__  
> You can use the wildcard character too... `ls *.txt`

`cd` - Change to directory specified by `<path>`

> __Optional Arguments:__  
> The location to move to... `cd <path>`

> __Special Characters:__  
> Move to the parent directory... `cd ..`  
> Return to previous working directory... `cd -`  
> Root of filesystem... `cd /`  
> Your home directory... `cd ~` or `cd --`  

---

`wget` - Download a file.

> __Required Arguments:__  
> File url... `wget <url>`

> __Hint:__  
> Try executing this... `wget http://www.gutenberg.org/cache/epub/2600/pg2600.txt`

> __Note for Mac Users:__  
> If you don't have `wget` try this... `curl -O  http://www.gutenberg.org/cache/epub/2600/pg2600.txt`

---

`cat` - Concatenate and print files

> __Required Arguments:__  
> The file to concatenate... `cat <file>`

> __Hint:__  
> Path multiple paths to concatenate files... `cat <file> <file>`

> __Special Characters:__  
> Send output to a new file... `cat file1.txt file2.txt > combined.txt`  
> Wildcards... `cat *.txt > all-the-files.txt`

---

`head` - Show the first ten lines of a file.

> __Required Arguments:__  
> The file to display... `head <file>`

> __Optional Flags:__  
> Specify `n` lines... head -n 25 <file>`

---

`tail` - Show the last ten lines of a file.

> __Required Arguments:__  
> The file to display... `tail <file>`

> __Optional Flags:__  
> Specify `n` lines... tail -n 25 <file>`

---

### Changing Things

`mkdir` - Make a new directory.  

> __Required Arguments:__  
> The name of the new directory... `mkdir <name>`

> __Optional Flags:__  
> Create intermediate directories as required. ... `mkdir -p <path>`  

`mv` - Move (or rename) a file or directory  

> __Required Arguments:__  
> The target and destination... `mv <target> <destination>`

`cp` - Copy a file or directory  

> __Required Arguments:__  
> The target and destination... `cp <target> <destination>`

> __Optional flags:__  
> Copy recursively (directories)... `cp -R`  

`rm` - Remove files and directories  

> __Required Arguments:__  
> The file or directory to remove... `rm <path>`

> __Optional Flags:__  
> Remove recursively (directories)... `rm -r`  

---

`open` - View directory or file specified by `<path>`.

> __Required Arguments:__  
> Directory or file... `open <path>`

> __Special Characters:__  
> A dot character refers to the current directory... `open .`

> __Note For Windows Users...__  
> Use this command instead... `explorer .`

`man` - Display documentation for a given command. _"Man" is short for "manual"._

> __Required Arguments:__  
> The command to display documentation for... `man <command>`

> __Hints:__  
> Exit a man page by pressing the 'q' key on your keyboard.

`history` - Show command history  
> __Special Characters:__  
> Recall previous command... `!!`  
> Repeat command in your history... `!<linenumber>`  
