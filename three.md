---
title: Week Three
---

### 3.1 | Introduction to Version Control With Git

Navigate to [try.github.io](https://try.github.io), and work through all the activities for a brief introduction to Git and it's commands that you will run through terminal.

This activity is relatively easy as the site will do the heavy lifting for you; please make an effort to read and understand what each command does.

### 3.2 | Install git on your computer
For Windows users only: install [Git for Windows](https://git-scm.com/download/win)


For Mac users only:
  - open terminal and type `git --version`
    - if there is a "command not found" message, install [Git for Mac](https://git-scm.com/download/mac)

### 3.3 | Create Your Own Version of a Template Repo (Git Fork)

- Log into GitHub using the account you signed up from Week 1
- Navigate to the [Code Cadets Git Template](https://github.com/eckersleyalexander/Code-Cadets-Git-Template)
- 'Fork' the repo by clicking on the button in the top right to make your own copy of the repository. **This will copy the entire repo and all its files onto your account.**

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/ForkButton.png" alt="Forking a repo" style="width: 100%;"/>

- Clone the repo to create a copy on your local machine. Go to Terminal, Navigate (cd) into the folder you wish to work from, and then run `git clone https://github.com/eckersleyalexander/Code-Cadets-Git-Template.git`. Replace the URL with your own one if you were able to fork your own repository.

- Open up the project in Atom.

### 3.4 | Bandit Challenge Cont.

- We will be continuing on with the Bandit challenge from [Week Two](two.md)
- Each time you discover a password, add it to the `Password.txt` file, in the folder for the level you are on.
- `git commit -am "write a descriptive message about what you changed here"` and `git push` it so you can save your progress.
- Try to get as far as you can by the end of the lesson.

### 3.4.1 | Bandit hints, tips and tricks

If you didn't start or forgot how to work with a remote server, here's a refresher.

- Open Terminal ssh into the bandit server of the level you're currently up to. To connect to level 0 type in `ssh bandit0@bandit.labs.overthewire.org -p 2220`.

- If you don't understand what this all means, we'll break it down for you.

 - `ssh` is the command you use to call the Secure Shell.

 - `banditX` where X is the number of the level you are on, is the username for the server. **This is the only part of the command that will change as you move to the next level.**

 - `@bandit.labs.overthewire.org` is the server address.

 - `-p 2220` is a parameter for the port you're connecting through.



<img src="https://canberragrammar.github.io/codecadets-2018/Resources/SSHStruct.png" alt="Structure of an SSH" style="width: 100%;"/>

- Once that has connected you'll be asked for a password. For level zero this is `bandit0`. You may notice while in Terminal that the password isn't typing; **it is there, there are just no onscreen characters as a security choice**.

 - For all other levels the password will be the one you found in the previous level (write it down to your a file in your local git repo so you don't lose it).

- Use the commands you've learnt in terminal and the ones suggested on the Challenge's website to find files containing the passwords to the next level.

- Remember to use the command `exit` to disconnect and logout before moving onto the next level.
