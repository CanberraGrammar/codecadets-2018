---

title: Week 4

---

### 4.1 | Pushing forwards with Git

Welcome back to another session in Git, quite possibly the most useful real world tool you'll learn with us.

If there are any Git concepts you don't remember, try looking over the content from [Week Three](three.md) before asking for help. By now you should be somewhat familiar with both navigating folders via Terminal and these useful git commands:

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

We don't expect you to know these all by heart though, it's a lot to remember, that's why we're giving them all to you here.

### 4.2 | Branching out

Up until now you've worked with Git as a basic change saving tool and for remote storage, not unlike saving a file to the cloud.

Now we want to start using Git to control versions of our project, and in future work together on the same programs. To do this, we will introduce Branches.

### 4.2.1 | What is a Branch?

A branch is a tool for controlling what exists within your project. It works exactly as the name would suggest; if you drew your project like a tree then a branch would come out the side.

Why would we want that? Well let's say we have a big App with lots of code, and that we want to add a new feature to it. We don't want the users of our App to see a half finished version, and we also risk making the original features not work.

So we need to create a development environment that is away from the live version. Here is a small sample of a project with one branch used for testing a new feature.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Branches.png" alt="What branches look like" style="width: 75%;"/>

In the above image, the Tree diagram depicts the structure of the repository's commit history, where the blue line depicts the main, "master" project, and the red line depicts a "Testing_Branch" that is off to the side. These two branches can be edited separately to each other by you or other users.

### 4.2.2 | Using branches

* Start by creating a new repository on your GitHub. If you go to https://github.com/ and are signed in you should see a New Repository button like so.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/NewRepo.png" alt="Creating a new Repo" style="width: 100%;"/>

**If you get stuck on any of the following steps, the commands are in the table at the top of the page!**

* Call it whatever you want, but make it something useful so you'll remember what it is later. Once created, clone your repo down onto your computer. You will need to copy and paste the link to your repo into the command.

* Add some basic text files or Python scripts of your own to the repo, and commit and push the changes.

* Create a new branch using `git checkout -b newBranchName` : Please replace newBranchName with a name of your choice.

* Edit some of the files within your git repo while in this branch. For this activity the contents of the file itself are not particularly important.

* Save and commit your changes.

### 4.2.3 | Merging together

* If you run `git branch` you will see a list of all active branches in your repo. Use a git checkout to get back onto the Master branch.

* Now we want to take the changes we made in the testing branch and put them into our main project. To do this, we will use `git merge branchName`. Push your changes to your remote repo.

* You have successfully created and merged a branch in Git. It may be difficult to appreciate the significance of your success at the moment, but this is one of the most important steps to collaborative development using Git.



### 4.3 | Conflicting messages

If you didn't quite get that section on branches then perhaps give it a re-read, as in this section we will be using them again. Next we want to observe what happens if multiple branches modified the same content when you want them to go back together.

* Create a new branch as we did before, and edit a file(s) in the repo. **You will then need to close the file in the editor for this activity.**

* Next, checkout back to your master branch and **edit the same file(s) you edited in the test branch, but change something different than last time!**.

* Try and merge your changes on the two branches together. You should get a warning along the lines of `fatal: Exiting because of an unresolved conflict.`

* Run up a `git status` to see what went wrong. It should tell you something similar to `both modified:   test.txt`.

* This is called a **"Merge Conflict"**, and if you work with others on the same code they can be quite a common problem.

### 4.3.1 | Resolving the conflict

* Open your test file in Atom. There should be a large box showing you where the merge conflict is; along with the buttons "Use me" for your changes and their changes.


<img src="https://canberragrammar.github.io/codecadets-2018/Resources/MergeConflict.png" alt="Merge conflicts" style="width: 100%;"/>

* Decide on which set of changes you want to keep. Either keep the Master changes, or accept and merge the test branch changes. Or you may want to take a combination of the two (you will have to remove the named markers, <<<<<, ===== and >>>>>).

* Once you've settled on a final version, save the file(s) and commit your changes back to the master branch, and push back to your remote. The branch will now be joined back to the master.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Conflict_Resolved.png" alt="Merge conflict resolved, branches rejoined" style="width: 75%;"/>

### 4.4 | Working Together

Last session we got you to fork your own copy of a remote repo, and then clone that down onto your machine. Today will be very similar, except you are going to directly clone one of our repos:

* `git clone https://github.com/AGellel/Code-Cadets-Week-4/`

* In this repo you should find a folder for the day of the week, and your class. Navigate to it, depending on your speed there may or may not be files in there already.

* Create a new branch exactly like we have before. Make the branch name your **Firstname-Lastname** so we know who it is.

* Create a new text or python file, and again name the file **Firstname-Lastname**, then add it to the repo and commit your changes.


* Now, try to push your changes to our remote. **<font color="red" > You should get an error message telling you  </font>**`fatal: The current branch branchName has no upstream branch.` The Terminal will tell you how to add a branch to the remote, see if you can do it yourself.

### 4.4.1 | Creating a Pull Request

Now that you've committed the changes to your branch, let's get it added to the Master branch of the project.

* Go back to https://github.com/AGellel/Code-Cadets-Week-4

* On the main page you should a button that says `New pull request.`

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/NewRequest.png" alt="Create a new pull request" style="width: 100%;"/>

* You will be taken to the following screen. Select your branch in the drop down menu labeled `compare`. If you don't see your branch, you likely failed to push it up.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/PullRequest.png" alt="The Request" style="width: 100%;"/>

* If your brach doesn't have any conflicts with existing files, it should merge it automatically. Once merged, check the repo's list of commits and you should be able to see yourself - if that is the case, go back over a few of the sections above.


<img src="https://canberragrammar.github.io/codecadets-2018/Resources/MergeSuccess.png" alt="Request successful" style="width: 100%;"/>

### 4.5 | Finishing up

Congratulations, you've successfully merged a new file using git into our project. Git is the foundation of most collaborative software work in the real world; and of all the things you'll learn with us over this year this is likely the most practical skill.

### 4.6 | Appendix - New Commands

Now that you've made it this far, here is a list of the git commands we've added to our knowledge in this session.

This could be a handy reference in future, although there will be plenty other sources on the internet you may want to use, such as [the GitHub Cheatsheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf).

| Command | Description |
|---------|-------------|
|git branch | List all branches in the repo. |
| git checkout -b branchName | Creates a new **branch** called branchName |
| git checkout branchName | Switches the repo to the branch called brachName|
| git merge branchName | **Merges** the changes in the specified branch. |
