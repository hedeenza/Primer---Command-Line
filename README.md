# Primer---Command-Line
A short and simple introduction to core command line commands and concepts

## Contents
1. Getting Your Bearings
    1.1. `whoami`
        1.1.1. !!! CRITICAL NOTE ABOUT SECURITY !!!
    1.2. `whatis`
    1.3. `echo`
    1.4. `pwd`
    1.5. Paths
        1.5.1. Absolute and Relative Paths
            1.5.1.1. `.`
            1.5.1.2. `..`
        1.5.2. Home (~)
        1.5.3. Root (/)
    1.6. `realpath`
    1.7. `ls`
    1.8. Command Options / Flags
    1.9. `ls` with Options
    1.10. Aside: File Permissions
    1.11. `clear`
    1.12. `cd`

## 1. Getting Your Bearings
Coming from a world of Graphic User Interfaces (GUIs) like Windows Explorer, the first time I (intentionally) opened a Command Line Interface (CLI) was incredibly intimidating. At first glance there's nothing there to explain what you're looking at, what you should be doing, or what's even possible. Only a couple characters and a blinking cursor stare back at you, silently awaiting your direction. This primer will only scratch the very surface of the vast and powerful possibilities when working with a CLI; but if all goes well, by the end you should be able to (1) know what kinds of questions to ask, (2) know where to find more help, (3) not feel like you're drowning while reading instructions that involve the command line.

This guide assumes you are using a Unix-like system such as macOS, Linux, the Windows Subsystem for Linux 2, or are using a tool such as Git Bash for Windows. The base Windows command line utility and Powershell often use quite different commands to execute the functionality described here, and will not be covered in this guide.

### 1.1. `whoami`
Getting started with the command line may have you feeling a bit existential. Thankfully, the terminal is there to help. Let's run your first command:  

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
