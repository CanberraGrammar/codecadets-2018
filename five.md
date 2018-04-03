---

title: Week 5

---

### 5.1 | Learning a new language

Welcome back for another week. We've now moved on from our Terminal and Git skills content back into some typical programming. Today we will be introducing you to C#, with the main idea being to help you adjust from Python's syntax.

##### So why learn C#?


* Easy answer: it's the primary language used by the Unity Game Engine which we will work in from Term 2.

* At present most of you are probably only familiar with Python. If you go on to study or work in Software you will work in many different languages. We aim to help you realise that all most languages are actually quite similar, so you're not starting from scratch


### 5.1.1 | Installing Mono

As C# is a language developed by Microsoft's .NET initiative, and as such it is not inherently compatible with Macs. We'll need some extra software if we want our terminal to be able to read it.

Follow this link [http://www.mono-project.com/download/stable/](http://www.mono-project.com/download/stable/ ) and select the current stable version.


<img src="https://canberragrammar.github.io/codecadets-2018/Resources/MonoStable.png" alt="Stable Version" style="width: 100%;"/>


Run and install the package. The installer will give you the instructions as usual.



### 5.2 | Programming Fundamentals

Most programming work can be easily divided down into 3 fundamental ideas.

* Sequence - things happen in the order they are written.

* Selection - decision making based on conditions, such as `if` and `else`.

* Iteration - doing things lots of times, such as `for` and `while` loops.

These 3 concepts are not language specific; you've learnt them all in Python, and they do not change in C#.

### 5.2.1 | Datatypes

In addition to this, majority of the datatypes you are already familiar with are universal to most languages.

| Datatype (common shorthand) | Description |
|---------|-------------|
| boolean (bool) | True or False. |
| integer (int) | Whole numbers (not decimals or fractions) |
| float | A 'floating point value', represents decimal numbers such as 2.2 or 3.14159 |
| character (chr/char) | Used to represent a single letter or symbol|
| String (str)| A list of characters |
| List | A ordered **list** of items of the same datatype paired with an index. |

### 5.3 | Transitioning into a new Syntax

Whilst the core concepts remain the same, their execution across various languages does not.

```Python
print('Hello World!') #This is Python
```

```c
Console.WriteLine("Hello World!"); //This is C#
```

Aside from the different instruction names, you might notice that C# code each line ends in a semicolon `;`. This is an important thing to remember when coming from Python, which does not use these to mark line ends.

### 5.3.1 | Making decisions

Below is a simple example of an If Else statement in the two languages. Both programs will output the same.

```Python
condition = True

if condition:
    print('The variable is set to true.')
else:
    print('The variable is set to false.')
#This is a Python If Else statement  
```

```c
bool condition = true;

if (condition) {
  Console.WriteLine("The variable is set to true.");
}
else {
  Console.WriteLine("The variable is set to false.");
} //This is a C# If Else statement
```

Notice a couple of key differences here.

* In C# we have to define the datatype of our variables, when in Python it is often implied. In this example, the variable `condition` is of the type boolean (true/false).

  * C# : `bool condition = true`

  * Python : `condition = True`

* In Python we use a `:` and Tab spacing to indicate what is contained inside the statement. In C# the block of code is contained by `{  }`.

### 5.3.2 | Looping around

The following two For Loops do the same thing. They print the numbers 1 to 10 to the console.

```Python
for i in range(1,11):
  print(i) #This is a python For Loop
```

```c
for (int i = 1; i < 11; i++) {
  Console.WriteLine(i);
}  //This is a C# For Loop
```

The C# For Loop syntax might look a little strange to you, so let's break it down a bit. After we initialise the loop we have 3 distinct parts.

* `int i = 1`  : Variable i of datatype **integer** is the starter of our loop counter. This is the bottom of the range() in the Python example.

* `i < 10`  : is our loop condition; in other words the loop will run only when i is less than 10. This is the top of the range() in the Python example,

* `i++`  : is a shorthand for i = i + 1. This is the rule by which the loop counter changes each run, sometimes known as the 'step'.


### 5.4 | Writing a C# Program

Using Atom create a new file. When you save it, use the file extension `.cs`, similar to how for python you'd use `.py`

<img src="https://canberragrammar.github.io/codecadets-2018/Resources/csExt.png" alt="C# .cs file extension" style="width: 50%;"/>

Now, in comparison to Python, you'll need some extra parts to run C# file successfully. Copy and paste this segment of code into yours before you start.

```cs
using System;

namespace MyProgram {
   class MyClass {
      static void Main(string[] args) {
        // YOUR CODE GOES IN HERE
        //
        //
        //
      }
    }
}
```

To test this write a basic program similar to the any of activities you'd have seen in Grok. What it does isn't too important, we just want to test that it runs on your system.

You may also want this command.

```Python
s = input(); #Input in Python
```

```cs
string s = Console.ReadLine(); //Read input in C#
```



### 5.4.1 | Running a C# Program (Mac OS)

C# compiles to a .exe format, which is great if you're on Windows; not so great for a Mac, as they have no native way to read them. That said, Mono is a great tool for both Mac and Windows to make life easier.

This is why we downloaded Mono earlier. Navigate in Terminal to the folder where your C# file is located and then run:

`mcs fileName.cs`

This will create from fileName.cs an executable called fileName.exe, which we can then execute from the Terminal with:

`mono fileName.exe`

The code should output to the Terminal just like a Python script would.



### 5.5 | C# Challenges

1. Write a program in C# that accepts a user input for a positive number called `n`, and then print all the numbers from `1` to `n`

2. Write a `FizzBuzz` program. It prints all numbers from 1 to 100, but every number divisible by 3 is replaced with `Fizz`, every number divisible by 5 is replaced with `Buzz`, and any number divisible by 3 AND 5 is replaced with `FizzBuzz`.

3. Write a program that takes user input for `height` and uses loops to output a pyramid made of asterisks of that height. E.g, the following pyramind is `height = 5`.

```
    *
   * *
  * * *
 * * * *
* * * * *
```


### 5.6 | Back to bandit

If you've finished everything else here feel free to return to the Bandit challenge from Weeks 2 and 3 to see how far you can get.
