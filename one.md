---
title: Week One
---

[//]: # (This is week one of the Code Cadets program)

### 1.1 | Introduction to Code Cadets & Setup

Hi there and welcome to Code Cadets this year! To start with, we'll get you up to speed with who your tutors are and what the Code Cadets program is all about.

You will have received an email about which group you are in, please make sure you are in the right session. If you need to change sessions due to a change in availability (Summer/Winter Sport etc...) please make sure you ask your parents to send through an email to your tutor.

This session will focus on setting up our computers and installing relevant programs we will be using. Please note there will be seperate instructions relevant to your type of computer; if you have a laptop running Windows, please navigate to this section (1.1.W1). If you have an Apple Macintosh, please navigate to this section (1.1.M1).

Our outcomes for this session are:
1. Familiarise yourselves with the Rules & Expectations
2. Install Atom
3. Install the Script package for Atom
3. Install a Linux Distribution (Windows Only)
4. Write a basic Python Program in Atom

### 1.1.W1 | Installing Atom (Windows)

Please note the following instructions are intended for students with **Windows** computers. If you have a Macintosh computer, please navigate to 1.1.M1

Firstly, navigate to https://atom.io/

Click on Download Windows 64-bit Installer.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Download_Atom_Windows.gif" alt="Drawing" style="width: 100%;"/>

Once you have successfully downloaded Atom, double click on the file and run the installation process.

### 1.1.W2 | Installing the Linux Subsytem (Windows)

Please note the following instructions are intended for students with **Windows** computers only. If you have a Macintosh computer, please navigate to 1.1.M1
We will be following the instructions listed on the Windows Official Website. (https://docs.microsoft.com/en-us/windows/wsl/install-win10).

Before beginning this step of the process, **Please ensure your windows is completely up to date, and that your version is the "Fall Creators Update" (Windows Build 16215) or later (To check your windows build, press Windows Key + R and type in "winver"). If it is not, please update windows before continuing.

Firstly, you need to open your start menu (Windows Key on your keyboard, or bottom left of your screen) and type in PowerShell. Right click the application and click run as Administrator.

The next step is to copy and paste in the following command line

```Python
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

It will then ask you if you would like to restart your computer. Please restart your computer by typing in "Y" and pressing return (don't worry, this page will still be here when you get back ^_^).

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Linux_Subsystem.gif" alt="Drawing" style="width: 100%;"/>

Our next step will be to download a Linux Distribution. We will be using Ubuntu in this course, but there are many other builds you could use.

Open up your start menu and type in Microsoft Store and launch the application.
Next search "Ubuntu" in the search field at the top right. Click on the relevant application and install it (this may take a while and have to be completed at home!).

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Ubuntu_Store.gif" alt="Drawing" style="width: 100%;"/>

### 1.1.M1 | Installing Atom (Macintosh)

Please note the following instructions are intended for students with **Macintosh** computers. If you have a Windows computer, please navigate to 1.1.W1

Firstly, navigate to https://atom.io/

Click on Download For Mac.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Download_Atom_Mac.gif" alt="Drawing" style="width: 100%;"/>

Once you have successfully downloaded Atom, double clip the downloaded .Zip file to "extract" the contents. Now drag the Atom Icon from your **Downloads** folder into your **Applications** folder.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Install_Atom_Mac.gif" alt="Drawing" style="width: 100%;"/>

To test you have installed it correctly, search for Atom using **Spotlight**. Spotlight is an extremely useful tool built into your Macintosh that can help you locate files and folders much faster than clicking through multiple UI elements. To use Spotlight, simply press Command + Space on your keyboard. This will bring up the Spotlight search bar, where you can enter "Atom" and then press return to open up Atom.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Spotlight_Search_Atom.gif" alt="Drawing" style="width: 100%;"/>

### 1.2 | Adding Packages to Atom 

Open up Atom. You should be taken to the main screen.

Now, we want to install an extra feature to Atom. The "Script" Package will allow us to run our code alongside our editor.

From the main screen, click "Install a Package", and then the blue "Open Installer" button. A new column should appear, containing a search bar. Enter "Script" into the search bar, and click the Enter key. After taking a moment to search, it should bring up the package, now simply click the "Install" button".

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/InstallScript.gif" alt="Drawing" style="width: 100%;"/>


### 1.3.1 | Making a new Script

Now that we can run our code, we need a script to test it on. To create a new file use the shortcut Command + N (Control + N on Windows). You should now have a blank window. Type in the following code:

```python
print("Hello World!")
```

Once you have entered this, Save the file with Command + S (Control + S on Windows). You will be asked for a file name, which should be "Hello.py". Save it to a folder that you'll remember.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/File_Name.png" alt="Drawing" style="width: 100%;"/>

### 1.3.2 | Running your Script

Now that you have written a basic program, let's run it. The fastest way to do this is Command + I (Control + I on Windows). At the bottom of your editor you should see a window that looks something like this.

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/Finished.png" alt="Drawing" style="width: 100%;"/>

If you see any Warnings or Errors, it's likely your code didn't run correctly, so double check your work and run it again.
