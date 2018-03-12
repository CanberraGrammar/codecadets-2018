---
title: Week Two
---

[//]: # (This is week two of the Code Cadets program)

### 2.1 | Background on Terminal / Linux Subsytem

**Relevant to Macintosh users only** Terminal is a Command Line Interface (CLI) application that provides you with text-based control of the operating system, subverting the traditional Graphical User Interface (GUI) provided to you in MacOS. It allows you to control aspects of your computer through text commands rather than interacting with graphical elements, giving you greater control and empowering you to do things you simply can't through the basic UI.

**Relevant to Windows users only** The Linux Subsytem is a way of emulating an instance of the Linux Operating System within Windows, allowing Windows users to have access to the Linux Console and the associated benefits of a fully fledged Command Line Interface (CLI) that were traditionally only available to Unix Based Operating Systems (MacOS & Linux) as Windows uses its own Windows **Kernel** (The [Kernel](https://en.wikipedia.org/wiki/Kernel_(operating_system)) is the program that manages all interactions between the software on your computer, and the physical hardware your computer has) that operates in a different manner to the Unix Kernel.

### 2.2 | Starting Up

If you are on a **Mac**, open Spotlight (Using the Command Key + Spacebar on your keyboard) and type in Terminal. An application will pop up, and this is what you will be using for the rest of this Lab.

If you are on **Windows**, open the start menu and type in Ubuntu, and launch the application. An application will launch and this is what you will use for the rest of the Lab.

**For All Students**, the following commands will be the basic commands we will be exploring throughout today's session. Don't focus on them too much for the time being, use this table throughout the session as a reference if you forget what something does.

A note on terminology;
1. Directory = Folder
2. A path is the path to a given directory
3. Command is what you type into Terminal
4. [bla] indicates that you replace [bla] with what you want, i.e. replace [name] with Alex.

| Command | Description |
|---------|-------------|
| cd [folder]| **Change Directory** to the given path |
| cd . .  | **Change Directory** up one level
| ls      | **List** the contents of the current directory |
| clear   | **Clears** the terminal window |
| mkdir [name]  | **Make Directory** with the given name |
| rm -R [path]  | **Remove** a given directory and it's contents |
| pwd | List the Directory you are currently in |
| whatis [command] | Gives you a description of a given command |


### 2.3 | Interacting with files

Now that you know how to navigate your directories, you can interact with files within them. To use our Hello World Python script from last week as an example. Firstly you'll need to cd into the directory where you saved the file, and then tell the computer to open it:

> open hello.py

However using this will open the file in its default program, often a basic Text-Editor. When you have additional editors, such as Atom, you probably don't want to open a file with its default program. To get around this, we can add parameter -a [App name] to our command to specify to the computer what program we want to use, like so:

> open -a "Atom" hello.py

If you wanted to view the file's contents directly in the command line, you can try:

> cat hello.py

### 2.3 | Running Code from Terminal

You can also run files for most programming languages directly from the Command Line.

> python hello.py

Some of you may have noticed last week that the Script plugin we use for Atom doesn't like Python's inline input instructions. If you have a program that uses these elements, running from Terminal is the best way to do it.

### 2.4 | Creating new files

Similar to making a new directory as shown in the table above, you can make new files directly from the command line. The touch command allows us to do just that.

> touch newFileName.py

Unless otherwise specified, this will be created inside the folder you are currently in. If the file shares a name with an existing file, it won't do anything.

### 2.5 | Putting it all together

Now that we have all these techniques, let's try and use them all to create and run a new Python script. If you can't remember how to do any of these steps, they're all detailed in the above sections.

**Remember to do this through the command line.**

1. Open a new Terminal/Ubuntu Window and navigate into the directory you want to work from.

2. Using mkdir in the table above, create a new folder for Code Cadets if you haven't already.

3. Create a new Python file (don't forget the .py extension), and then open it in Atom via the command line.

4. Edit your code in Atom and save the file.

5. Run your code from the command line to test that it compiles.

For the Python code, you can use just use this sample below, similar to what you'll have seen in Grok, or you can make your own script to do whatever you want.

```Python
name = input("What is your name? ")
print("Hello, " + name + "!")
```


### 2.6 | _________
