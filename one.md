---
title: Week One
---

[//]: # (This is week one of the Code Cadets program)

### 1.1 | Introduction to Code Cadets & Setup

Hi there and welcome to Code Cadets this year! To start with, we'll get you up to speed with who your tutors are and what the Code Cadets program is all about.

You will have received an email about which group you are in, please make sure you are in the right session. If you need to change sessions due to a change in availability (Summer/Winter Sport etc...) please make sure you ask your parents to send through an email to your tutor.

This session will focus on setting up our computers and installing relevant programs we will be using. Please note there will be seperate instructions relevant to your operating system.

Select the operating system your laptop is running:


[<img src="https://canberragrammar.github.io/codecadets-2018/Resources/apple.png" alt="Apple Icon"/> MacOS](#Mac)
[<img src="https://canberragrammar.github.io/codecadets-2018/Resources/windows.png" alt="Windows Icon"/>Windows](#Windows)


Our outcomes for this session are:
1. Familiarise yourselves with the Rules & Expectations
2. Install Atom
3. Install Python 3
4. Install the Script package for Atom
5. Install a Linux Distribution (Windows Only)
6. Write a basic Python Program in Atom

<a name="Windows"></a>

### 1.1.W1 | Installing Atom (Windows)

Please note the following instructions are intended for students with **Windows** computers. If you have a Macintosh computer, please navigate to [(1.1.M1)](#Mac).

Firstly, navigate to [https://atom.io/](https://atom.io/)

Click on Download Windows 64-bit Installer.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Download_Atom_Windows.gif" alt="Downloading Atom" style="width: 100%;"/>

Once you have successfully downloaded Atom, double click on the file and run the installation process.

### 1.1.W2 | Installing the Linux Subsytem (Windows)

Please note the following instructions are intended for students with **Windows** computers only. If you have a Macintosh computer, please navigate to [(1.1.M1)](#Mac).
We will be following the instructions listed on the Windows [Official Website](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

Before beginning this step of the process, **Please ensure your windows is completely up to date**, and that your version is the "Fall Creators Update" (Windows Build 16215) or later (To check your windows build, press Windows Key + R and type in "winver"). If it is not, please update windows before continuing.

Firstly, you need to open your start menu (Windows Key on your keyboard, or bottom left of your screen) and type in PowerShell. Right click the application and click run as Administrator.

The next step is to copy and paste in the following command line

```Python
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

It will then ask you if you would like to restart your computer. Please restart your computer by typing in "Y" and pressing return (don't worry, this page will still be here when you get back).

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Linux_Subsystem.gif" alt="Activating Optional Feature" style="width: 100%;"/>

Our next step will be to download a Linux Distribution. We will be using Ubuntu in this course, but there are many other builds you could use.

Open up your start menu and type in Microsoft Store and launch the application.
Next search "Ubuntu" in the search field at the top right. Click on the relevant application and install it (this may take a while and have to be completed at home!).

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Ubuntu_Store.gif" alt="Downloading Ubuntu" style="width: 100%;"/>

### 1.1.W3 | Installing Python (Windows)

The final setup step is to install the Python programming language. If you already have Python installed, you can skip this step.

Navigate to the [Python website]("http://wwww.python.org") and download the latest version of Python 3.X.X

Once you have downloaded the installer, simply open the executable and click through the steps.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/py_windows.gif" alt="Installing Python" style="width: 100%"/>

<a name="Mac"></a>

The Windows-specific setup should be complete, head over to section [1.2](#Packages) to continue.

### 1.1.M1 | Installing Atom (Macintosh)

Please note the following instructions are intended for students with **Macintosh** computers. If you have a Windows computer, please navigate to 1.1.W1

Firstly, navigate to https://atom.io/

Click on Download For Mac.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Download_Atom_Mac.gif" alt="Downloading Atom" style="width: 100%;"/>

Once you have successfully downloaded Atom, double clip the downloaded .Zip file to "extract" the contents. Now drag the Atom Icon from your **Downloads** folder into your **Applications** folder.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Install_Atom_Mac.gif" alt="Installing Atom" style="width: 100%;"/>

To test you have installed it correctly, search for Atom using **Spotlight**. Spotlight is an extremely useful tool built into your Macintosh that can help you locate files and folders much faster than clicking through multiple UI elements. To use Spotlight, simply press Command + Space on your keyboard. This will bring up the Spotlight search bar, where you can enter "Atom" and then press return to open up Atom.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Spotlight_Search_Atom.gif" alt="Using Spotlight" style="width: 100%;"/>

### 1.1.M2 | Installing Python (Macintosh)
In order to run the program you are about to write, you must install python 3. Download and install the [latest version of python](https://www.python.org/ftp/python/3.6.4/python-3.6.4-macosx10.6.pkg). Follow the steps to install python 3, ask the tutors about any errors you encounter.

The Macintosh-specific setup should be complete, head over to section [1.2](#Packages) to continue.

<a name="Packages"></a>

### 1.2 | Sign up for GitHub

The last thing we need to set up for use in the code cadets program will be to create a GitHub account. GitHub is a version control system we will be exploring a little bit later in the term. GitHub is a widly used industry tool for managing software projects, it allows you to keep detailed logs of the changes your project undergoes during developments, and lets you roll back if something goes wrong.

This entire website is hosted through GitHub and you can check out the repo [here.](https://github.com/CanberraGrammar/codecadets-2018)

Visit the [GitHub Sign up Page](https://github.com/join) to begin the sign up process.
For your email address, use your school email address (in the format firstname.lastname@cgs.act.edu.au). Your user name must be in the format CGS-Firstname-Lastname (for example, John Smith will have an email address of john.smith@cgs.act.edu.au and a username of CGS-John-Smith).

You can add in an avatar and customize your profile page, but bear in mind this is a public profile and you are representing the school publically so the picture you choose and any information you decide to add should be appropriate.



### 1.3 | Adding Packages to Atom

Open up Atom. You should be taken to the main screen.

Now, we want to install an extra feature to Atom. The "Script" Package will allow us to run our code alongside our editor.

From the main screen, click "Install a Package", and then the blue "Open Installer" button. A new column should appear, containing a search bar. Enter "Script" into the search bar, and click the Enter key. After taking a moment to search, it should bring up the package, now simply click the "Install" button".

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/InstallScript.gif" alt="Adding Packages" style="width: 100%;"/>


### 1.4.1 | Making a new Script

Now that we can run our code, we need a script to test it on. To create a new file use the shortcut Command + N (Control + N on Windows). You should now have a blank window. Type in the following code:

```Python
print("Hello World!")
```

Once you have entered this, Save the file with Command + S (Control + S on Windows). You will be asked for a file name, which should be "Hello.py". Save it to a folder that you'll remember.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/File_Name.png" alt="Making a Python file" style="width: 100%;"/>

### 1.4.2 | Running your Script

Now that you have written a basic program, let's run it. The fastest way to do this is Command + I (Control + I on Windows). At the bottom of your editor you should see a window that looks something like this.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Finished.png" alt="Running a Python file" style="width: 100%;"/>

If you see any Warnings or Errors, it's likely your code didn't run correctly, so double check your work and run it again.

### 1.5 | Summary

By now you should have achieved the following:
- Installed Atom (Windows & Mac Students)
- Installed the Linux Subsystem (Windows Students)
- Install Python (Windows & Mac Students)
- Signed up for a GitHub account (Windows & Mac Students)

If you have not yet completed one of these activities, please go back and make sure you have. If you are having any troubles with one of the steps, please talk to your tutor or ask one of the mentors.

### 1.6 | Python Challenge

Once you've completed the guide *and* read through the rules of engagement guide, start working through these challenges. If you haven't coded before chuck your hand up and your tutor will step through getting started with you. Complete these as you go and try and rack up as many points as you can by the end of today.

1. Write a program that loops through from 1 to 100 (5 pts)
2. Write a program that prints out all fibonacci numbers from 1 to 100 (20 pts)
3. Push some code to a new repository on GitHub (10 pts)
4. Print out some kind of table using ASCII characters in Python (20 pts) e.g.:

```
\
 \
  \
   \
    \
     \
      \
_______\
```

