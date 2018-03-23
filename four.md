---

title: Week 4

---

### 4.1 | Progress with Git

Welcome back to another session in Git, quite possibly the most useful tool you'll learn with us.

If there are any concepts you don't remember, try going back over the content from [Week Three](three.md) before asking for help.

By now you should be somewhat familiar with both navigating folders via Terminal and these useful git commands:

| Command | Description |
|---------|-------------|
| git init | **Initialise** a new local repository |
| git status | Gives the **Status** of the current local repository (the one on your machine).
| git add fileName | **Add** the file called fileName to the repo.|
| git add --all | **Add all** files to the git repo. |
| git commit -am "message goes here"      | **Commits** the current set of changes. Think of it like saving. |
| git push | **Pushes** your commits to the remote repository (the one stored on GitHub)|
| git clone URL | **Clones** the the repository at the **URL** you give the command, for example the GitHub address of the repo.
| git pull | **Pulls** other commits down from the remote repo onto your local repo. |

### 4.2 | Branching out

Up until now you've worked with Git as a basic change saving tool and for remote storage, not unlike saving a file to the cloud.

Now we want to start using Git to control versions of our project. And we will start with Branches.

### 4.2.1 | What is a Branch?

A branch is a tool for controlling what exists within your project. It works exactly as the name would suggest; if you drew your project like a tree then a branch would come out the side.

Why would we want that? Well let's say we have a big App with lots of code, and that we want to add a new feature to it. We don't want the users of our App to see a half finished version, and we also risk making the original features not work.

So we need to create a development environment that is away from the live version. Here is a small sample of a project with one branch used for testing a new feature.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Branches.png" alt="What branches look like" style="width: 100%;"/>

### 4.2.2 | Using branches

* Start by creating a new repository on your GitHub. If you go to https://github.com/ and are signed in you should see a New Repository button like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/NewRepo.png" alt="Creating a new Repo" style="width: 100%;"/>

* Call it whatever you want, but make it something useful so you'll remember what it is later. Once created, clone your repo down onto your computer. You will need to copy and paste the link to your repo into the command.

* `git checkout -b newBranchName` : Please replace newBranchName with a name of your choice.

### 4.3 | Conflicting messages

If you didn't quite get that section on branches then perhaps give it a re-read, as in this section we will be using them again.


* Try and merge your changes. You should get a warning along the lines of `fatal: Exiting because of an unresolved conflict.`

* Run up a `git status` to see what went wrong. It should tell you something like `both modified:   test.txt`.

* Open your test file in Atom. There should be a large box showing you where the merge conflict is.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/MergeConflict.png" alt="Merge conflicts" style="width: 100%;"/>

### 4.4 | Asking Nicely

Last time we got you to fork your own copy of a remote repo, and then clone that down onto your machine. Today will be very similar, we are going to:
