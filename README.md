# Primer---Command-Line
A short and simple introduction to core command line commands and concepts

## Contents
1. Getting Your Bearings
    1.1. `whoami`
        1.1.1. !!! CRITICAL NOTE ABOUT SECURITY !!!
    1.2. `echo`
    1.3. `whatis`
    1.4. `pwd`
    1.5. Paths
        1.5.1. Root (/)
        1.5.2. Absolute and Relative Paths
            1.5.3.1. `.`
            1.5.3.2. `..`
        1.5.3. Home (~)
    1.6. `ls`
    1.7. Command Options / Flags
    1.8. `man`
    1.9. `ls` with Options
    1.10. Aside: File Permissions
    1.11 `realpath`
    1.12. `clear`
    1.13. `cd`

## 1. Getting Your Bearings
Coming from a world of Graphic User Interfaces (GUIs) like Windows Explorer, the first time I (intentionally) opened a Command Line Interface (CLI) was incredibly intimidating. At first glance there's nothing there to explain what you're looking at, what you should be doing, or what's even possible. Only a couple characters and a blinking cursor stare back at you, silently awaiting your direction. This primer will only scratch the very surface of the vast and powerful possibilities when working with a CLI; but if all goes well, by the end you should be able to (1) know what kinds of questions to ask, (2) know where to find more help, (3) not feel like you're drowning while reading instructions that involve the command line.

This guide assumes you are using a Unix-like system such as macOS, Linux, the Windows Subsystem for Linux 2, or are using a tool such as Git Bash for Windows. The base Windows command line utility and Powershell often use quite different commands to execute the functionality described here, and will not be covered in this guide.

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

If you just need a quick answer to "what does this command do?" it's a nice option. Most commands come with a built in manual containing much more information about its function. We'll cover that in 1.9.

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
### 1.8. `man`
### 1.9. `ls` with Options
### 1.10. Aside: File Permissions
### 1.11 `realpath`
### 1.12. `clear`
### 1.13. `cd`
