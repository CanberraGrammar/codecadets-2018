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
