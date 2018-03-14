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
| cat [file] | Print out the contents of a given file |
| pwd | List the Directory you are currently in |
| cat [filename] | Print out the contents of a given file |
| whatis [command] | Gives you a description of a given command |

### 2.2 | Navigating directories

Two commands you will end up using the most often are **ls** & **cd**. ls will list all the files & folders in the current directory you are in and cd will allow you to change directories. Typing cd followed by a directory will take you there. If you are confused or not sure where to go next, you can type ls to see all the current folders and files that are inside the folder you are currently in. For example, you could type:

```Python
cd Documents
```
to be taken to your documents folder.

Lets give it a try:

**Mac Only** - Your task is to navigate to your desktop in terminal using the cd command (Hint: try using ls to start).

**Windows Only** - When you first open your Ubuntu window, you will be in the home directory of your *Ubuntu instance*. However, you want to be able to access your Windows files, so when you open up the window you need to type:

```Python
cd /mnt/c
```

cd being change directores, mnt being the list of all your *mounted drives* and c being the typical letter asigned to your boot drive (if you open My Computer, you will see your hard drive labelled as Local Disck C).


### 2.4 | Interacting with files

Now that you know how to navigate your directories, you can interact with files within them. To use our Hello World Python script from last week as an example. Firstly you'll need to cd into the directory where you saved the file, and then tell the computer to open it:

```python
open hello.py
```

However using this will open the file in its default program, often a basic Text-Editor. When you have additional editors, such as Atom, you probably don't want to open a file with its default program. To get around this, we can add parameter -a [App name] to our command to specify to the computer what program we want to use, like so:

```python
open -a "Atom" hello.py
```

If you wanted to view the file's contents directly in the command line, you can try:

```python
cat hello.py
```

### 2.5 | Running Code from Terminal

You can also run files for most programming languages directly from the Command Line.

```python
python hello.py
```

Some of you may have noticed last week that the Script plugin we use for Atom doesn't like Python's inline input instructions. If you have a program that uses these elements, running from Terminal is the best way to do it.

### 2.6 | Creating new files

Similar to making a new directory as shown in the table above, you can make new files directly from the command line. The touch command allows us to do just that.

```python
touch newFileName.py
```

Unless otherwise specified, this will be created inside the folder you are currently in. If the file shares a name with an existing file, it won't do anything.

### 2.7 | Putting it all together

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


### 2.8 | SSH (Secure Shell)

SSH is a way for you to be able to log into another computer (generally a server) remotely, and be presented with a Unix Based CLI to control the computer. This is a tool that you will certainly use if you continue on with Computer Science into University or practice it in the real world.

You need 3 things to log into a remote client using SSH.
- The ssh URL
- Username
- Password

For example, at the Australian National University, you can log into the computer lab computers from home to access all your saved documents/access tools that are installed on the university computers. The way we do this is by typing the follow into our Terminal window (uXXXXXXX being the username, and partch.anu.edu.au being the ssh URL):

```python
ssh uXXXXXXX@partch.anu.edu.au
```
Please note that this is just an example and won't actually run for you.

We then are prompted for our university password, and then we can access the university computers through our terminal windows, and perform commands such as copying over files to our local machine. To end an ssh session, you would simply type:

```Python
exit
```

### 2.9 | Challenge Activity | Over the Wire: Bandit

For the remainder of this session, you will be working your way though a series of challenges designed to test your understandings of the concepts above. You must read each page carefully, and use the hints they give you if you want to make any progress.

The aim is to use your critical thinking, and your new found knowledge of Bash commands to find the password for the next level. To progress to the next level, you must end the ssh session and log in again using the new password.

**You must end the ssh session with the exit command before attempting to log in again using the new password.**

[http://overthewire.org/wargames/bandit/](http://overthewire.org/wargames/bandit/)


Note: the remote server may feel a little laggy and unresponsive at times.
