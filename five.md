---

title: Week 5

---

### 5.1 | Learning a new language

Welcome back for another week.

### 5.1.1 | Why learn C#?

Easy answer: it's the primary language used by the Unity Game Engine.

At present most of you are probably only familiar with Python.


### 5.1.2 | Installing Mono (Mac OS)




### 5.2 | Programming Fundamentals

Most programming work can be easily divided down into 3 fundamental ideas.

* Sequence - things happen in the order they are written.

* Selection - decision making based on conditions, such as `if` and `else`.

* Iteration - doing things lots of times, such as `for` and `while` loops.

These 3 concepts are not language specific; you've learnt them all in Python, and they do not change in C#.

### 5.3 | Transitioning into a new Syntax

Whilst the core concepts remain the same, their execution across various languages does not.

```Python
print('Hello World!') #This is Python
```

```c
Console.WriteLine("Hello World!"); //This is C#
```

-----

### 5.3.3 | Looping around

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

The C# For Loop syntax might look a little strange to you, so let's break it down a bit. After we intialise the loop we have 3 distinct parts.

* `int i = 1`  : Variable i of datatype **integer** is the starter of our loop counter. This is the bottom of the range() in the Python example.

* `i < 10`  : is our loop condition; in other words the loop will run only when i is less than 10. This is the top of the range() in the Python example,

* `i++`  : is a shorthand for i = i + 1. This is the rule by which the loop counter changes each run.


### 5.4 | Running a C# Program.

C# compiles to a .exe format, which is great if you're on Windows; not so great for a Mac, as they have no native way to read them.

This is why we downloaded Mono earlier. Navigate in Terminal to the folder where your C# file is located and then run:

`mcs fileName.cs`

This will create from fileName.cs an executable called fileName.exe, which we can then execute from the Terminal with:

`mono fileName.exe`

### 5.5 | C# Challenges
