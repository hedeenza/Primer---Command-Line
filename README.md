# Primer - Command-Line
A short and simple introduction to core command line commands and concepts

## Contents
0. [Introduction](https://github.com/hedeenza/Primer---Command-Line#0-Introduction)  
1. [Getting Your Bearings](https://github.com/hedeenza/Primer---Command-Line#1-getting-your-bearings)  
    1.1. [`whoami`](https://github.com/hedeenza/Primer---Command-Line#11-whoami)  
    1.1.1. [!!! CRITICAL NOTE ABOUT SECURITY !!!](https://github.com/hedeenza/Primer---Command-Line#111-critical-note-about-security-)  
    1.2. [`echo`](https://github.com/hedeenza/Primer---Command-Line#12-echo)  
    1.3. [`whatis`](https://github.com/hedeenza/Primer---Command-Line#13-whatis)  
    1.4. [`pwd`](https://github.com/hedeenza/Primer---Command-Line#14-pwd)  
    1.5. [Paths](https://github.com/hedeenza/Primer---Command-Line#15-paths)  
        1.5.1. [Root (/)](https://github.com/hedeenza/Primer---Command-Line#151-root-)  
        1.5.2. [Absolute and Relative Paths](https://github.com/hedeenza/Primer---Command-Line#152-absolute-and-relative-paths)  
            1.5.2.1. [`.`](https://github.com/hedeenza/Primer---Command-Line#1521-)  
            1.5.2.2. [`..`](https://github.com/hedeenza/Primer---Command-Line#1522-)  
        1.5.3. [Home (~)](https://github.com/hedeenza/Primer---Command-Line#153-home-)  
    1.6. [`ls`](https://github.com/hedeenza/Primer---Command-Line#16-ls)  
    1.7. [Command Options / Flags](https://github.com/hedeenza/Primer---Command-Line#17-command-options--flags)  
        1.7.1. [Aside: File Permissions](https://github.com/hedeenza/Primer---Command-Line#171-aside-file-permissions)  
    1.8. [`man`](https://github.com/hedeenza/Primer---Command-Line#18-man)  
    1.9. [`ls` with Options](https://github.com/hedeenza/Primer---Command-Line#19-ls-with-options)  
    1.10. [`clear`](https://github.com/hedeenza/Primer---Command-Line#110-clear)  
    1.11. [cd](https://github.com/hedeenza/Primer---Command-Line#111-cd)  
        1.11.1. [Aside: Tab Completion](https://github.com/hedeenza/Primer---Command-Line#1111-aside-tab-completion)  
        1.11.2. [Going Home](https://github.com/hedeenza/Primer---Command-Line#1112-going-home)  
    1.12. [`realpath`](https://github.com/hedeenza/Primer---Command-Line#112-realpath)  
    1.13. [`history`](https://github.com/hedeenza/Primer---Command-Line#113-history)  
    1.14. [Conclusion: Part 1](https://github.com/hedeenza/Primer---Command-Line#114-conclusion-part-1)  
2. [Working With Files](https://github.com/hedeenza/Primer---Command-Line#2-working-with-files)  
    2.1. [`which`](https://github.com/hedeenza/Primer---Command-Line#21-which)  
    2.2. [`mkdir`](https://github.com/hedeenza/Primer---Command-Line#22-mkdir)  
    2.3. [`touch`](https://github.com/hedeenza/Primer---Command-Line#23-touch)  
    2.4. [`rm`](https://github.com/hedeenza/Primer---Command-Line#24-rm)  
        2.4.1. [!!! NEVER RUN THE FOLLOWING !!!](https://github.com/hedeenza/Primer---Command-Line#241--never-run-the-following-)  
    2.5. [`mv`](https://github.com/hedeenza/Primer---Command-Line#25-mv)  
    2.6. [`cp`](https://github.com/hedeenza/Primer---Command-Line#26-cp)  
    2.7. [Wildcards](https://github.com/hedeenza/Primer---Command-Line#27-wildcards)  
    2.8. [Pipes](https://github.com/hedeenza/Primer---Command-Line#28-pipes)  
    2.9. [`cat`](https://github.com/hedeenza/Primer---Command-Line#29-cat)  
    2.10. [`head`](https://github.com/hedeenza/Primer---Command-Line#210-head)  
    2.11. [`tail`](https://github.com/hedeenza/Primer---Command-Line#211-tail)  
    2.12. [`wc`](https://github.com/hedeenza/Primer---Command-Line#212-wc)  
    2.13. [`sort`](https://github.com/hedeenza/Primer---Command-Line#213-sort)  
    2.14. [`grep`](https://github.com/hedeenza/Primer---Command-Line#214-grep)  
    2.15. [Text Editors - Nano + Vim](https://github.com/hedeenza/Primer---Command-Line#215-text-editors---nano--vim)  
    2.16. [Conclusion: Part 2](https://github.com/hedeenza/Primer---Command-Line#216-conclusion-part-2)  
  
## 0. Introduction
Coming from a world of Graphic User Interfaces (https://github.com/hedeenza/Primer---Command-Line#GUIs) like Windows Explorer, the first time I (intentionally) opened a Command Line Interface (CLI) was incredibly intimidating. At first glance there's nothing there to explain what you're looking at, what you should be doing, or what's even possible. Only a couple characters and a blinking cursor stare back at you, silently awaiting your direction. This primer will only scratch the very surface of the vast and powerful possibilities when working with a CLI; but if all goes well, by the end you should be able to (1) know what kinds of questions to ask, (2) know where to find more help, (3) not feel like you're drowning while reading instructions that involve the command line.

This guide assumes you are using a Unix-like system such as macOS, Linux, the Windows Subsystem for Linux 2, or are using a tool such as Git Bash for Windows. The base Windows command line utility and Powershell often use quite different commands to execute the functionality described here, and will not be covered in this guide.

## 1. Getting Your Bearings

### 1.1. `whoami`
Getting started with the command line may have you feeling a bit existential. Thankfully, the terminal is there to help. Let's run your first command. Type the following and press enter:  

```
$ whoami
```

#### 1.1.1. **!!! CRITICAL NOTE ABOUT SECURITY !!!**
If you just ran that command without reading ahead or knowing exactly what it does, ***I strongly urge you to never do that again.*** With the command line you have a level of control over your system like you've never had before, especially as the "root user". Running commands you find on the Internet (especially if you commit a "cardinal security sin" of "piping curl into bash" `curl <some-link> | sh`, which is essentially running arbitrary commands you're blind to on your device) may be totally safe or it may allow mailicious actors to take control of your system and signed-in accounts, compromise your network, install malware, steal your access-keys, files, and other sensitive information, ransom your device, and more without you ever realizing. Please be very careful, but do not let that awareness stop you from learning. Knowledge is a key to keeping you and your device(s) safe while using them with their full potential.

Note about `$`: I will prefix commands with a `$`. This is a common representation of the command line when you're NOT the "root user", a special user with elevated permissions to do anything on your device, often represented by `#`. You may see something different on your device, like a `>`, but it should all work the same. The outputs of commands in this guide will be prefixed by `>`, and will appear below the command that produced it.

Back to our existential moment...

```
$ whoami
> your-username
```

By running the `whoami` command, you should get your username back (or "root" if you're signed in as the root user). There are times it's useful to be able to check.

### 1.2. `echo`
Now that we know who we are, let's shout into the void and see what comes back. 

```
$ echo hello?
> hello?

$ echo hello?!
> hello?!

$ echo hello!!!
> hello!!!
```

`echo` is a command that prints a line of text. The text we provided after the command is an "argument". `echo` seems like a boring command when you use it this way, but if you get into scripting with the command line, `echo` can be used to print messages or the outputs of your commands to the terminal where you can see them, which is handy for both knowing what's happening with your program and testing.

If you didn't *just know* what `echo` would do, how could you find out? Of course you could look it up online, but there are other tools for determining what commands are and how they work that are likely built right into your terminal.

### 1.3. `whatis`
The first command that can help you learn what a command does is `whatis`. This command, followed by the name of the command you'd like to learn more about, will return a "one-liner" about the command's function.

```
$ whatis echo
> echo (1)             - display a line of text
```

We can even run this command on itself:

```
$ whatis whatis
> whatis (1)           - display one-line manual page descriptions
```

If you just need a quick answer to "what does this command do?" it's a nice option. Most commands come with a built in manual containing much more information about its function. We'll cover that in 1.8.

### 1.4. `pwd`
We know who we are, and there doesn't seem to by anything around. How do we find out where we are? We can print our "working directory" (or "the folder you're currently looking in") to the terminal:

```
$ pwd
> /home/username
```

The output of this command may look different depending on your system. It may read something more like `/Users/username`, but in either case, it shows the "Path" of where you are in your file system.

### 1.5. Paths
Paths are like directions. They tell you how to get from one place to another. Each directory (folder) along the way is like a fork in the road and is separated from the next fork by a `/`. If you got directions to go from home to work in this format, they may look something like: `/home/main-street/highway/exit15/fourth-street/work`

#### 1.5.1. Root (/)
The root of your file system is represented by `/`. This is the directory that contains everything* else on your device.

* Well not *everything* but that's outside of the scope of this primer.

#### 1.5.2. Absolute and Relative Paths
Absolute Paths start from the root, while Relative Paths start from your current working directory. In our directions analogy, the absolute path from home to work is `/home/main-street/highway/exit15/fourth-street/work`, but if you're at Exit 15, your Relative Path to work is `./fourth-street/work`

##### 1.5.2.1. `.`
A `.` refers to your working directory, wherever that currently is. If your working directory is `highway/`, `.` refers to highway.

##### 1.5.2.2. `..`
A `..` refers to the parent directory of your working directory, wherever that currently is. If you're in your `work/` directory, the parent directory is the directory that contains `work/`, in this case, `fourth-street/`.

#### 1.5.3. Home (~)
We refer to our "home directory" so often there is a convenient shortcut to represent it: `~`. Instead of writing out the entire file path from the root, if you ever see a path like `~/Documents/`, you know it's referring to the Documents directory located in your home directory.

### 1.6. `ls`
All of that in mind, let's see what our working directory contains. I always think of this as the "list stuff" command:

```
$ ls
> Desktop Documents Downloads Music Pictures Videos
```

Your output may look different, but it is likely that your home directory contains the default, primary directory's we're familiar with, plus anything else you've saved to this directory. Directories may be displayed with a trailing forward-slash (`Desktop/`) or their text may be colored differently, or each item may look exactly the same depending on your settings.

### 1.7. Command Options / Flags
I've always found this view of directory contents crowded. Let's add a "flag" to our command and see what happens.

```
$ ls -l
> Permissions   Size    User        Date Modified   Name
> drwxr-xr-x       -    user-name   01-01-1999      Desktop
> drwxr-xr-x       -    user-name   01-01-1999      Documents
> ...
```

By adding the `-l` flag, or "option", we see the same content as before but with additional details. The "Permissions" column can be seen as a representation of "what kind of file is this, and who is allowed to do what with this file". "Size" is the file size (does not display for directories). "User" is the owner of the file. "Date Modified" is when the file or directory contents were last changed. "Name" is the name of the file or directory.

Most command line tools utilize flags to alter their functionality in some way. Flags are not consistent across tools. For example, the `-l` flag we just added to `ls` will not have the same effect on the `whatis` command, and `echo` does not have an `-l` flag at all.

#### 1.7.1. Aside: File Permissions
File permissions are represented by a 10-character string. The first character tells you what kind of file it is: `.` for a file, `d` for a directory, and sometimes `l` for a link. The following 9 characters are divided into groups of 3. The first 3 refer to the User, the middle 3 to the Group, and the last 3 to Others. There are 4 common characters: `r`, `w`, `x`, and `-`. You may also see an `s` or `t` where the `x`'s are. You can learn more about those cases in [this article](https://www.redhat.com/en/blog/suid-sgid-sticky-bit) by Redhat. `r` means the specified individuals are able to *read* the file. `w` means the specified individuals are able to *write* to the file. `x` means the specified individuals are able to *execute* the file. `-` means the specified individuals are not able to perform that action.

As an element of a comprehensive security plan, there's a concept known as "least permissions". This means everything should have as few enabled permissions as possible while still allowing the file to perform the necessary functions, with the knowledge that you can change permissions later. That way files that aren't supposed to be accessed in certain ways have at least a little protection from accidents or malicious actors. We'll discuss changing permissions later, but if you're curious about this topic I encourage you to explore more.

Note: Directories are a special case. You need to be able to "execute" them to open them. 

### 1.8. `man`
How did we know that `ls` even had that option? Are we condemned to need to memorize every possible option of every possible command we could ever need? No! You likely have access to a manual for almost every single command available to you on the command line through the `man` command. The format is `man <command-you-want-to-learn-about>`

```
$ man ls
> Name
> ...
> Synopsis
> ...
> Description
> ...
> Author
> ...
> Reporting Bugs
> ...
> Copyright
> ...
```

Running this command provides us with all of the details for using the specified command. The "Synopsis" section will often contain the "format" the command takes. For example, `ls [OPTION]... [FILE]...` means that after the `ls` command, you will optionally list any flags/options you want (found in the "Description" section), and then optionally add a file (more likely a directory) to list the contents of. We have the hint that these additions are optional because they are [written in square brackets].

Many options have both "short" and "long" forms. The short forms will often consist of a dash (sometimes read as "tack") and a single case-sensitive character. Long forms will consist of two dashes and a full word. Both forms work the same way, you enter them differently when you're using more than one. Sometimes short form options can be grouped together on a single dash, like `-cvf` after the `tar` command, where the long forms would require separation, like `--create --file <OUTPUT_FILE> --verbose <INTPUT_FILE>`.

You can navigate man pages with the up and down arrow keys, or in some cases using Vim-like bindings. We'll briefly discuss Vim later, but here are a few bare-bones commands to help you comfortably move around the manual:

- q = quit
- j = Move down
- k = Move up
- gg (pressing the G key twice) = Move to the top of the page
- G (Shift + G) = Move to the bottom of the page
- / = Open the search option. Type the word you'd like to search for and press ENTER.
- n = Cycle forward through search results.
- N = Cycle backward through search results.

### 1.9. `ls` with Options
Let's try running `ls` with another option. This time we'll use the flag right at the top of the list. Adding this flag will also list the "hidden" files whose names begin with a period. Note that we could have used `ls --all` to produce the same result.

```
$ ls -a
> ...
> .bash_history
> .bashrc
> ...
```

We can combine multiple short flags into one block with the `ls` command as well.

```
$ ls -la
> Permissions   Size    User        Date Modified   Name
> ...
> .rw-r--r--       -    user-name   01-01-1999      .bash_history
> .rw-r--r--       -    user-name   01-01-1999      .bashrc
> ...
```

### 1.10. `clear`
The terminal is looking pretty crowded. Let's clear some space.

```
$ clear
```

In some cases this command will not truly "clear" the screen, but rather shift the display up, allowing you to "scroll back" to where you were before.

### 1.11. `cd`
We've learned several tools so far. We know who we are (`whoami`), where we are (`pwd`, Paths), what's here (`ls`), and how to learn what our commands do (`whatis`, `man`). Now it's time to venture from Home. Let's "change directory" into our "Documents".

```
$ cd Documents
```

From here we can run all the same commands as before to get a lay of the land. We can double check that we are where we think we are with `pwd` (though many terminals display at least a partial working directory path before your equivalent `$`), or list what's here with `ls`. Practice the commands you've learned so far by exploring your file system on the command line.

Note that you do not need to run `cd` once for each directory "layer". If you know where you want to go, you can string the names together in one command, separated by `/`.

```
$ cd Documents/Program_A/Project_B/Task_C
```

#### 1.11.1. Aside: Tab Completion
You may have long directory names. Typing them out exactly in full each time can become incredibly tedious. Tab completion is here to help. When you've typed enough of a file or directory name that it could "unambiguously point to only one thing", you can press the TAB key and it should complete the name for you. If you hit TAB and there are multiple matches, it may complete "as far as it can" and then list potential matches. Some terminals allow selection of the matches, while others do not. This can take a little while to get used to, but it's life changing when you do.

#### 1.11.2. Going Home
Wait, we've gone as far as we can and there are no more directories to `cd` into. How do we go back? There are two main options. The first is a little more tedious but will allow us to review an important use of relative file paths. This command will bring you to the parent directory of your current directory ("up one layer").

```
$ cd ..
```

We could repeat this process over and over again to get back home:

```
$ cd ..
$ cd ..
$ cd ..
...
```

Or we could use `/` to indicate that we want to go to the parent directory of the parent directory of the... and so on.

```
$ cd ../../../and so on..
```

We may not always want to go all the way back home. Sometimes we may want to go to, or refer to a directory that is in the parent directory. In that case we can use our knowledge of relative file paths:

```
$ cd ../../Task_C/Item_D
```

When it is time to go home, wherever we are in our file system, we can get there in one step.

```
$ cd ~
```

### 1.12. `realpath`
If you ever need to get the full file path of any file, you can use the `realpath` command.

```
$ realpath spreadsheet.csv
> /home/username/Documents/Program_A/Project_B/Task_C/Item_D/spreadsheet.csv
```

### 1.13. `history`
We've run a lot of commands so far. If you ever want to refer back to a command you've previously run, you can do so with `history`.

```
$ histroy
> Number   Command
> ...
```

### 1.14. Conclusion: Part 1
With what we've covered so far, you should always know where you are and how to get anywhere in your file system. If you forget a command you've run, you can find it in your history; and if you don't know what a command does or what its available options are, you can get a short or a long explanation right from your device. In the next section we'll cover some basics of working with files and file management in the command line so that once you've gone where you need to go you can start taking action.

## 2. Working With Files

### 2.1. which
How do we know whether we have access to a command line program or not?

```
$ whatis which
> which (1)            - shows the full path of (shell) commands.

$ which which
> /usr/bin/which
```

If you have the command installed, the terminal will return the path to the command. If you do not, it will return something like "No <COMMAND> in (PATH)". The Path is a long string of absolute paths separated by `:`'s. This represents everywhere your terminal looks for the commands you enter. We'll cover how to add directories to your path in Part 3.

### 2.2. mkdir
In this section we'll be creating, altering, and deleting directories and files. Navigate to somewhere you'd like to store the files for this section using the skills you learned in Part 1. Then we'll make a new directory. You can name it whatever you'd like.

```
$ mkdir directory_name
```

Navigate into the directory and we'll run the rest of the commands from there.

### 2.3. touch
We can create a new empty file named "file_name" with the `touch` command. You don't need a file extension, but you can add one like `.txt` if you prefer.

```
$ touch file_name
```

### 2.4. rm
Be ***extremely careful and absolutely certain*** with this command. Unlike moving a file to the Trash Bin in a GUI environment, there is no way to retrieve the file or directory once you have deleted it in this manner. 

We can remove files with `rm`.

```
$ rm file_name
```

If we try to run `rm` on a directory, we will get an error. Using the `-r` / `--recursive` flag will allow us to irrevocably delete a directory ***and all of its contents***.

```
$ rm -r directory_name
```

#### 2.4.1. ***!!! NEVER RUN THE FOLLOWING !!!***
The following command is extremely dangerous. It forces the irrevocable recursive deletion of everything in your root directory, meaning everything on your device. There are some memes about running this command, so use this knowledge for recognition, but please never run this yourself.

```
!!! DO NOT RUN THIS COMMAND !!!
$ rm -rf /
!!! DO NOT RUN THIS COMMAND !!!
```

### 2.5. mv
Let's create another directory.

```
$ mkdir second_directory
```

We can move the `file_name` file into this directory with `mv`.

```
$ mv file_name second_directory
```

We can check that the file did indeed move where we think it did using `ls`

```
$ ls
> second_directory

$ ls second_directory
> file_name
```

We can also use `mv` to rename a file

```
$ mv file_name new_name
```

### 2.6. cp
We can copy a file using the `cp` command

```
$ cp new_name new_file

$ ls 
> new_name new_file
```

### 2.7. Wildcards

### 2.8. Pipes
There are 3 kinds of "pipes" we'll discuss. Pipes are used to take the output of one command and use it in some way. The `>` pipe will *replace* the contents of the destination with the output of your command. The `>>` pipe will *append* the output of your command to the destination, adding to rather than replacing. The `|` pipe takes the output of one command and uses it as the input for the following command.

Note: If you see yourself utilizing the command line frequently or for more advanced uses, I strongly recommend learning more about standard in ("stdin"), standard out ("stdout"), and standard error ("stderr").

The following will add the text `Hello, World` to `new_file`

```
$ echo "Hello, World!" > new_file
```

!!! If we run the command again with different text and the same pipe, it will replace the old text with our new text. ***This can be dangerous*** because though the examples only use a single line of text, you can accidentally replace the entire file's contents with as little as a single character using this pipe and not have any way of returning to the original contents. Please be careful with this pipe.

The following will add the text `This is a new line` to `new_file` rather than replacing `Hello, World~`

```
$ echo "This is a new line" >> new_file
```

We'll examine the usage of `|` soon.

### 2.9. cat
We can use the `cat` command to print out the contents of our file.

```
$ cat new_file
> Hello, World!
> This is a new line
```

### 2.10. head
If you have a very long file and only want to examine the beginning rather than see the whole things, we use `head`.

```
$ head very_long_file
> Line 1
> Line 2
> Line 3
> Line 4
> Line 5
> Line 6
> Line 7
> Line 8
> Line 9
> Line 10
```

You can specify the number of lines with with `-n` flag.

```
$ head -n 5 very_long_file
> Line 1
> Line 2
> Line 3
> Line 4
> Line 5
```

### 2.11. tail
We can do something similar but with the end of the file using `tail`

```
$ tail very_long_file
> Line 991
> Line 992
> Line 993
> Line 994
> Line 995
> Line 996
> Line 997
> Line 998
> Line 999
> Line 1000
```

### 2.12. wc

### 2.13. sort

### 2.14. grep

### 2.15. Text Editors - Nano + Vim

### 2.16. Conclusion: Part 2

