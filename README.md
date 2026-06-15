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
    2.8. [`rename`](https://github.com/hedeenza/Primer---Command-Line#28-rename)  
    2.9. [Pipes](https://github.com/hedeenza/Primer---Command-Line#29-pipes)  
    2.10. [`cat`](https://github.com/hedeenza/Primer---Command-Line#210-cat)  
    2.11. [`head`](https://github.com/hedeenza/Primer---Command-Line#211-head)  
    2.12. [`tail`](https://github.com/hedeenza/Primer---Command-Line#212-tail)  
    2.13. [`wc`](https://github.com/hedeenza/Primer---Command-Line#213-wc)  
    2.14. [`sort`](https://github.com/hedeenza/Primer---Command-Line#214-sort)  
    2.15. [`file`](https://github.com/hedeenza/Primer---Command-Line#215-file)  
    2.16. [`grep`](https://github.com/hedeenza/Primer---Command-Line#216-grep)  
    2.17. [Text Editors - Nano + Vim](https://github.com/hedeenza/Primer---Command-Line#217-text-editors---nano--vim)  
    2.18. [Conclusion: Part 2](https://github.com/hedeenza/Primer---Command-Line#218-conclusion-part-2)  
3. [Downloads, Executables, and `.bashrc`]()
    3.1. [`curl`](https://github.com/hedeenza/Primer---Command-Line#31-curl)
    3.1.1. [!!! CARDINAL SECURITY SINS !!!]()
    3.2. [`wget`](https://github.com/hedeenza/Primer---Command-Line#32-wget)
    3.3. [`sha256sum`](https://github.com/hedeenza/Primer---Command-Line#33-sha256sum)
    3.4. [`b2sum`](https://github.com/hedeenza/Primer---Command-Line#34-b2sum)
    3.5. [`gpg`](https://github.com/hedeenza/Primer---Command-Line#35-gpg)
    3.6. [`chmod`](https://github.com/hedeenza/Primer---Command-Line#36-chmod)
    3.6.1. [Executing Scripts]()
    3.7. [`env`](https://github.com/hedeenza/Primer---Command-Line#37-env)
    3.8. [`.bashrc`]()
    3.8.1. [Adding Directories to Your Path]()
    3.8.2. [Command Aliases]()
    3.9. Conclusion: Part 3
4. [Where To Go From Here]()
    4.1. [Additional Commands That Are Worth Knowing]()
    4.2. [Other Command Line Methods]()
    4.3. [Taking The Time To Learn Vim / Neovim]()
    4.4. [Resources]()
  
## 0. Introduction
Coming from a world of Graphic User Interfaces (GUIs) like Windows Explorer, the first time I (intentionally) opened a Command Line Interface (CLI) was incredibly intimidating. At first glance there's nothing there to explain what you're looking at, what you should be doing, or what's even possible. Only a couple characters and a blinking cursor stare back at you, silently awaiting your direction. This primer will only scratch the very surface of the vast and powerful possibilities when working with a CLI; but if all goes well, by the end you should be able to (1) know what kinds of questions to ask, (2) know where to find more help, (3) not feel like you're drowning while reading instructions that involve the command line.

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

### 2.1. `which`
How do we know whether we have access to a command line program or not?

```
$ whatis which
> which (1)            - shows the full path of (shell) commands.

$ which which
> /usr/bin/which
```

If you have the command installed, the terminal will return the path to the command. If you do not, it will return something like "No <COMMAND> in (PATH)". The Path is a long string of absolute paths separated by `:`'s. This represents everywhere your terminal looks for the commands you enter. We'll cover how to add directories to your path in Part 3.

### 2.2. `mkdir`
In this section we'll be creating, altering, and deleting directories and files. Navigate to somewhere you'd like to store the files for this section using the skills you learned in Part 1. Then we'll make a new directory. You can name it whatever you'd like.

```
$ mkdir directory_name
```

Navigate into the directory and we'll run the rest of the commands from there.

### 2.3. `touch`
We can create a new empty file named "file_name" with the `touch` command. You don't need a file extension, but you can add one like `.txt` if you prefer.

```
$ touch file_name
```

### 2.4. `rm`
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

### 2.5. `mv`
Let's create another directory.

```
$ mkdir second_directory
```

We can move the `file_name` file into this directory with `mv`.

```
$ mv file_name second_directory
```

We can check that the file did indeed move where we think it did using `ls`.

```
$ ls
> second_directory

$ ls second_directory
> file_name
```

We can also use `mv` to rename a file.

```
$ mv file_name new_name
```

### 2.6. `cp`
We can copy a file using the `cp` command.

```
$ cp new_name new_file

$ ls 
> new_name new_file
```

### 2.7. Wildcards
Sometimes you'll want to perform actions with multiple files rather than just one or one at a time. The `*` wildcard will match from zero to any number of characters. The `?` wildcard will match exactly one character. Let's create a couple files to help us.

```
$ touch file_a.txt
$ touch file_b.txt
$ touch file_c.txt
$ touch a.md
$ touch b.md
$ touch c.csv
$ touch d.csv
```

Let's say we wanted to "select" only the files ending in `.txt`. We can accomplish that with `*`.

```
$ ls *.txt
> file_a.txt file_b.txt file_c.txt
```

In this instance, we could accomplish the same using the `?` wildcard, because the `?` will match any single character.

```
$ ls file_?.txt
> file_a.txt file_b.txt file_c.txt
```

We can create a "class" of possible values by placing them inside square brackets.

```
$ ls file_[ac].txt
> file_a.txt file_c.txt
```

Or a "range" of possible values using the square brackets.

```
$ ls file_[a-c].txt
> file_a.txt file_b.txt file_c.txt
```

We can use a wildcard more than once.

```
$ ls *a*
> file_a.txt a.md
```

Or mix and match.

```
$ ls *[ad]*
> file_a.txt a.md b.md d.csv
```

Though we have only been listing the files that match our descriptions, you use this same pattern matching when performing actions like moving files or searching through each a particular kind of file with a command like `grep`.

### 2.8. `rename`
I don't know about you, but there has been a time or two I realized I had several files to rename and then sat there dreading how much tedious work it would be. The dread certainly scales with the number of files there are. If I knew about `rename` back then I could have saved a ton of time.

```
$ ls
> old_file.txt
$ rename "old" "new" "old_file.txt"
$ ls 
> new_file.txt
```

With the `-a` flag we can replace every instance of our target, which can be useful for times when you need to do things like replace every space in a file name with `_`.

```
$ rename -a " " "_" "a rather long and tedious file name.txt"
$ ls
> a_rather_long_and_tedious_file_name.txt
```

These commands don't have any guards on them, so you need to be absolutely sure about the change you're making. Those times that you're not 100% sure and want to check, we can use `-n --verbose` to see what change will take place without actually making the change.

```
$ rename -n --verbose "txt" "md" file_a.txt
> `file_a.txt' -> `file_a.md'
```

Using what we learned about wildcards, we can apply changes like these to several files at once. Here's an example from the man page for a situation where you have files named "`file1`, `file2`, ... `file9`, `file10`, ..., `file278`, ..." The following will add a "00" between the recurring "file" name and any single digit, matched with `?`.

```
$ rename "file" "file00" "file?"
```

Then we can do something similar for the file names with double digits.

```
$ rename "file" "file0" "file??"
```

Now all of our files have 3 digits after the file name (`file001`, `file002`, ..., `file010`, ..., `file278`).

### 2.9. Pipes
There are 3 kinds of "pipes" we'll discuss. Pipes are used to take the output of one command and use it in some way. The `>` pipe will *replace* the contents of the destination with the output of your command. The `>>` pipe will *append* the output of your command to the destination, adding to rather than replacing. The `|` pipe takes the output of one command and uses it as the input for the following command.

Note: If you see yourself utilizing the command line frequently or for more advanced uses, I strongly recommend learning more about standard in ("stdin"), standard out ("stdout"), and standard error ("stderr").

The following will add the text `Hello, World` to `new_file`.

```
$ echo "Hello, World!" > new_file
```

!!! If we run the command again with different text and the same pipe, it will replace the old text with our new text. ***This can be dangerous*** because though the examples only use a single line of text, you can accidentally replace the entire file's contents with as little as a single character using this pipe and not have any way of returning to the original contents. Please be careful with this pipe.

The following will add the text `This is a new line` to `new_file` rather than replacing `Hello, World!`.

```
$ echo "This is a new line" >> new_file
```

We'll examine the usage of `|` soon.

### 2.10. `cat`
We can use the `cat` command to print out the contents of our file.

```
$ cat new_file
> Hello, World!
> This is a new line
```

### 2.11. `head`
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

### 2.12. `tail`
We can do something similar but with the end of the file using `tail`.

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

### 2.13. `wc`
Sometimes you'll want information about the text in a file. `wc` by default will display the number of lines, number of words, and byte count of a file.

```
$ wc file.txt
> 674 5644 35149 file.txt
```

You can isolate the line count with `-l`, the word count with `-w`, the character count with `-m`, or the number of characters in the longest line with `-L`. When run on multiple files using the wildcards we learned, it will also print a total.

```
$ wc -l *
> 0 file_a.txt
> 0 file_b.txt
> 0 file_c.txt
> 0 a.md
> 0 b.md
> 0 c.csv
> 0 d.csv
> 0 total
```

### 2.14. `sort`
Command outputs can be messy. Fortunately we can sort the standard output of a command by piping it into the `sort` command. For this example, we'll first add a few lines to `file_a.txt`.

```
$ echo "These" >> file_a.txt
$ echo "are" >> file_a.txt
$ echo "a" >> file_a.txt
$ echo "few" >> file_a.txt
$ echo "lines" >> file_a.txt
```

Then we'll check that the contents are what we think they are.

```
$ cat file_a.txt
> These
> are
> a
> few
> lines
```

Now we can try sorting the output.

```
$ cat file_a.txt | sort
> a
> are
> few
> lines
> These
```

We can reverse the output with `-r`.

```
$ cat file_a.txt | sort -r
> These
> lines
> few
> are
> a
```

There are several more options available to `sort` that may be useful depending on your sorting needs.

### 2.15. `file`
If a file does not have a file extension it may be unclear what kind of file it really is. We can use the `file` command to find out.

```
$ file file_a.txt
> file_a.txt: ASCII text
```

If you're ever working with a file that you don't trust for whatever reason, you may be surprised that `file` returns a different file type that you were expecting.

```
$ file suspicious.txt
> suspicious.txt: PE32+ executable for MS Windows 5.02 (console)...
```

I am certainly neither qualified to give you cybersecurity advice regarding what to do should this happen, nor to claim that a file is definitely safe if it does return what you are expecting, but it is always best to proceed with caution.

### 2.16. `grep`
When we want to find something but can't remember which file it's in, `grep` is a go to tool. There are several powerful options available and I encourage you to read about them in the man page. Using `grep` will generally take the form:

```
$ grep [OPTIONS] "what-to-search" "where-to-search"
```

Some useful options include:
- `-A #` - print # lines after the match
- `-B #` - print # lines before the match
- `-C #` - print # lines surrounding the match
- `-e` - Enable REGEX pattern matching for the "what-to-search" string.
- `-i` - Make the search case-insensitive.
- `-l` - Only print the names of the files that have matches.
- `-L` - Only print the names of the files that DO NOT have matches.
- `-n` - Include the line number of the file where there is a match.
- `-r` - Recursively search each subdirectory 

"Where to search" can include wildcards, allowing you to take such actions as "recursively searching through all of the '.log' files for a certain keyword, like "Time", ignoring capitalization, and printing the line numbers of the matched lines.

```
$ grep -rin "Time" *.log
```

### 2.17. Text Editors - Nano + Vim
I remember being surprised to learn that there are text editors built right into most terminal emulators. Two of the most ubiquitous are Nano and Vim. Nano is known for being a little more "beginner friendly". Note that the `^` notation by the commands at the bottom of the screen correspond to either the `CTRL` or `Command` keys depending on your device. `^Q` is therefore activated by pressing `CTRL` and `Q`  together (`CTRL + Q`).

```
$ nano file_a.txt
```

We can open the file with Vim as well. If you need to exit Vim without saving any changes, the command is `:qa!` (you do need to type the colon character `:`). If this doesn't work right away, press `<ESC>` a couple times first and then retry. Some of the most popular Vim memes are about people not being able to exit. I didn't know either the first few times I opened a document with Vim and needed to close my entire terminal.

```
$ vi file_a.txt
```

The use of each of these text editors is well beyond the scope of this primer, but I wanted you to know that they were there. Vim has an intense learning curve, but it's well worth the effort. The initial experience almost everyone has with Vim is "my keyboard stopped functioning", but once you've learned and practiced "Vim Motions" and cycling between the "normal", "insert", and "visual" modes, as well as learned how to create and run "macros", you'll be surprised at the speed and power at your fingertips. An added bonus is that several programs (like Obsidian md) and Integrated Development Environments (IDEs) have an option to enable Vim Motions, so the speed and fluency you learn can be applied elsewhere.

### 2.18. Conclusion: Part 2
I hope that at this point you feel much more confident with the command line than you were when you started. You may not be best friends yet, but just like all relationships, your relationship with the command line will take time and go through several ups and downs before you fully understand each other. While the beginning may have felt intimidating, so far you've:

- Explored over 20 common commands
- Learned how to check if a command is available 
- Learned how to learn what those commands do
- Understood Paths
- Learned how to move around freely
- Understood file permissions
- Utilized Pipes
- Learned how to perform basic interactions with files

In Part 3 we'll cover a couple more essential commands and concepts concerning running command line tools you write yourself or find online.

## 3. Downloads, Executables, and `.bashrc`

### 3.1. `curl`
`curl` is a command for downloading things from the Internet. The man page for curl is a novel, or at 39,219 words, technically a [novella](https://en.wikipedia.org/wiki/Novella).

```
$ man curl | wc -w
> 39219
```

There's a ton `curl` can do, and a lot of it may not be relevant to you. In the interest of keeping this guide short, I encourage you to look for external resources for more on this command. There are a ton of videos on YouTube *just* about how to use `curl`. But to get you started, the basic form of the command is:

```
$ curl <some-link>
```

#### 3.1.1. !!! CARDINAL SECURITY SINS !!!
The instructions for acquiring many popular tools ask that you "pipe curl into bash". These include: [The Rust Language](https://rust-lang.org/tools/install/), [Homebrew](https://brew.sh/), [uv](https://docs.astral.sh/uv/#installation), and [Tauri](https://tauri.app/). This command flow downloads whatever exists at the link to your device using `curl`, and then immediately runs it using `sh`. Even if the source is trusted there is a risk that the download itself could have been compromised. The command will look like one of the following:

```
!!! RUN WITH EXTREME CAUTION !!!
$ curl <some-link> | sh
$ sh <(curl <some-link>)
!!! RUN WITH EXTREME CAUTION !!!
```

If there are no other options for installing the tool, what are you to do? The simplest remedy for the situation is to break up the commands and not use the pipe. Download the installer script with `curl`, carefully inspect the element for what it's doing, and once you've determined nothing suspicious is going on, *then* run the script with `sh`. If you are a mostly non-technical command line user, you may be thinking "Great, now I can look at it but I don't know what's actually going on here." If you cannot verify yourself you must do some offloading of trust to someone else. We'll discuss more about verifying downloads in *3.3. `sha256sum`* and *3.5. `gpg`*. 

Note that malicious changes can seem relatively innocuous at first. In the [hijacking of orphaned packages on the Arch User Repository](https://thehackernews.com/2026/06/over-400-arch-linux-aur-packages.html), scripts were changed to use `npm` to download a malicious package that ran when the package was built. They even made it look like the changes were made by "a long-standing maintainer, an account an Arch Linux Trusted User later confirmed was never compromised."

Often the installer scripts for tools like this are available on [GitHub](https://github.com/). A search for "<Tool Name> github" should bring up a link to the project repository if there is one. After confirming that the installer script on GitHub is the same one you downloaded (or just downloading/copy-pasting the GitHub version to be sure), you can find the "Blame" for the code, which includes time stamps, who made the changes, and often a note about the changes. If it is a popular tool and there haven't been any very recent changes, there is a chance you can proceed without worrying too much. Popular tools with a lot of eyes on them tend to make changes quickly even if something malicious happens. This is of course no guarantee, but it's one more method for making sure you know what's happening before you download.

### 3.2. `wget`
`wget` is another tool for downloading things from the Internet. Much like `curl` there are several options and capabilities. The basic form of the command is:

```
$ wget <some-link>
```

### 3.3. `sha256sum`
A one-way cryptographic hashing function.
One-way meaning we can generate a consistent output from a known input, but cannot determine the input from the output.
64 character alpha-numeric string.
A way to check the integrity of a download.
Does not guarantee the safety of a file, but can help you know that you have downloaded what you intended to.
Very sensitive to changes.

```
$ echo "this sentence will become the input for our hashing function" | sha256sum
> 3211369cb4c274c87533289faf9379b49f658cd8835df1a78e6f44b5deb2e7e8
```

We can see how much making the first letter a capital changes the resulting value.

```
$ echo "This sentence will become the input for our hashing function" | sha256sum
> 2d3ce1feb9e3d2a2f03eb14eee8443a93dd5dc028e05a8392b8e770512047dae
```

Getting the sha256 checksum for a file.

```
$ sha256sum <FILE>
> <some-alphanumeric-string>
```

Sometimes downloads will be accompanied by a file to check the sha256sums against so you don't have to compare the values manually. With some files there are even checksums *for the checksums files*! We can create a file to check against using pipes.

```
$ sha256sum <FILE> >> sha256sums.txt
```

We can check the hashes of each of the files in the working directory against our file using the `-c` option.

```
sha256sum -c sha256sums.txt
> FILE: OK
```

### 3.4. `b2sum`
The `b2sum` is similar to the `sha256sum` but uses a different algorithm. You may see a `b2sum` hash listed in addition to or alongside a `sha256` checksum.

### 3.5. `gpg`
Signing

### 3.6. `chmod`
We can change the permissions of files using the `chmod` command. Generally commands will take the following form:

```
$ chmod who (permit-or-restrict) what <File>
```

Who can be the User (`u`), Group (`g`), Other(`o`), or All(`a`). We can add permissions with `+` and remove them with `-`. The basic permissions we can specify are Read(`r`), Write(`w`), and Execute(`x`). For example, if we want to "add executable permissions for the user to a file":

```
$ chmod u+x <FILE>
```

We can stringing multiple changes together at once with `,`. The following will add execute permissions for the user while also adding write and execute permissions for the group.

```
$ chmod u+x,g+wx <FILE>
```

We can set permissions quickly using [octal notation](https://en.wikipedia.org/wiki/Chmod). For example, the first command of the following sets the User to being able to read-write-execute, the Group to read-write, and Other to read-only (`.rwxrw-r--`); the second command sets the User to read and execute, and everyone else to none (`.r-x------`):

```
$ chmod 764 <FILE> 
$ chmod 500 <FILE> 
```

#### 3.6.1. Executing Scripts
Shell scripts
`$ sh executable_file.sh`
Binary executables
`$ ./executable_file`

### 3.7. `env`
Some tools may require the creation or editing of environmental variables. For an alphabetized list of your current environmental variables:

```
$ env | sort
> VARIABLE=value
> ...
```

### 3.8. `.bashrc`
The `.bashrc` file is a hidden file that lives in your home directory. When you start a terminal session, every command in your `.bashrc` is run, effectively meaning that changes you make here will be persistent after you close your terminal. Your terminal emulator may use a `.zshrc` for this same purpose.

#### 3.8.1. Adding Directories to Your Path
There are times when you will want your terminal to look in more places for commands than it does by default. We can add lines like the following to our `.bashrc` file to that end. This will allow us to run our own commands from anywhere, just like we do the commands that are already built into your device. We can add additional lines whenever we want our terminal to look in additional directories for commands.

```
# An optional comment explaining why you added this to your PATH
export PATH="$PATH:/home/user-name/path/to/desired/directory"
```

#### 3.8.2. Command Aliases
Sometimes the full command name for a command we install or write ourselves can be burdensome to type over and over, even with tab completion. We can create an alias to let our terminal know that when we type our custom abbreviation, we really mean to run the intended command. 

```
alias something_short="a_much_longer_or_undesirable_command" # Any desired notes for your later reference?
```

I always like to check that I'm not creating an alias that is actually a different command by running `which something_short` first and seeing if my intended alias returns something unexpected.

### 3.9. Conclusion: Part 3

## 4. Where To Go From Here
At the beginning of this guide we set out to achieve the following by the end:

1. Know what kinds of questions to ask
2. Know where to find more help
3. Not feel like you're drowning while reading instructions that involve the command line.

I hope that by introducing a range of tools, core concepts like options and safety, and `man` pages, you feel you know enough that you can search for help effectively and understand what you're reading when you find it.

If you so choose this is just the beginning of a much longer the journey with the command line.

### 4.1. Additional Commands That Are Worth Knowing
There are *so* many useful commands and you'll stumble upon ways of using even familiar tools that will blow your mind over and over again. 

- `comm` - compare two sorted files line by line
- `diff` - compare files line by line
- `git` - version control system
- `gzip` / `gunzip` - compress or expand files
- `ln` - make links between files (including symbolic links, which assist the "I wish this file was here but I can't / shouldn't actually move it here" problem).
- `ps`, `top` - report a snapshot of the current processes.
- `rsync` - a fast, versatile, remote (and local) file-copying tool
- `sed` - stream editor for filtering and transforming text
- `ssh`, `ssh-keygen`, `ssh-agent`, `ssh-copy-id` - OpenSSH remote login client, handling SSH keys. Here's a [video to get started](https://www.youtube.com/watch?v=YS5Zh7KExvE).
- `tar` - an archiving utility

### 4.2. Other Command Line Methods
- Redirecting with `<`
- Process substitution `<()`

### 4.3. Taking The Time To Learn Vim / Neovim
While the first stages of learning Vim are intense and unintuitive, I do strongly recommend learning it if you're going to spend an appreciable amount of time programming, coding, or otherwise editing text with a keyboard. The speed and freedom Vim Motions and Vim macros can provide are unmatched, and they're available in more places than you'd think. There are certain tasks I would have either thought impossible, or at least taken far more time than they were worth, had it not been for he capabilities of Vim.

### 4.4. Resources 
- [W3 Schools Bash Tutorial](https://www.w3schools.com/bash/index.php)
- [The Complete Bash Scripting Course](https://www.youtube.com/watch?v=Sx9zG7wa4FA) by [You Suck at Programming](https://www.youtube.com/@yousuckatprogramming)
- [The Primeagen's Vim As Your Editor Series Intro](https://www.youtube.com/watch?v=X6AR2RMB5tE)
