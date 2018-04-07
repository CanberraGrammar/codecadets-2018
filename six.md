---

title: Week 6

---

### 6.1 | End of Term

Welcome back once more for the last time this Term. By now you have probably learnt various basic Software skills such as a the Terminal and Git, and are familiar with basic programming techniques.

Today we won't be introducing any new concepts. It's the last week of term, everyone's mind is likely on the holidays ahead. So instead we're going to get you to go over some programming challenges to help improve your ability to read and write C#, so that when we move onto Unity it's more familiar to you.



You do not have to do these in any particular order. If you get stuck on one feel free to try another.


#### Reminder

For your C# programs you will need this in your code body.

```cs
using System;

namespace MyProgram {
   class MyClass {
      static void Main(string[] args) {
        // !!!!!!YOUR CODE GOES IN HERE!!!!!!!
        // The "//" makes a comment
        // Any commented line of code won't run
      }
    }
}
```

### 6.2 | Selection challenges

1. Write a program in C# that asks the user for their name, and then


### 6.3 | Iteration Challenges

1. Write a program in C# that accepts a user input for a positive number called `n`, and then print all the numbers from starting from `1` up to `n`.

2. Write a program that accepts a user input for a positive number called `n`, and then print all the numbers from staring from `n` down to `1`.

3. Write a program that takes user input for `height` and uses loops to output a triangle made of asterisks (with spaces in between each) of that height. E.g, the following pyramid is `height = 5`.



```
*
* *
* * *
* * * *
* * * * *
```
For a more difficult challenge, try and make the triangle into a pyramid like so. The following example is also of `height = 5`. Your code should still work for **any possible height**.

```
    *
   * *
  * * *
 * * * *
* * * * *
```


### 6.4 | Putting stuff together

These challenges will require you to use loops **AND** if statements to complete.

1. Write a `FizzBuzz` program. It prints all numbers from 1 to 100, but every number divisible by 3 is replaced with `Fizz`, every number divisible by 5 is replaced with `Buzz`, and any number divisible by 3 AND 5 is replaced with `FizzBuzz`.


### 6.5 | C# References

Looking for a reminder of what a certain operation looks like in C#? Look no further, here are all the tasks you'd probably want for today's session, but of course, there's always other ways to solve a problem.

```cs
//The following is examples of different code elements in C#
using System;

namespace MyProgram {
   class MyClass {
      static void Main(string[] args) {

        //Output/print
        //With line break
        Console.WriteLine("Hello World!");
        //Without line break
        Console.Write("Hello World!");
        //Concatenation
        string name = "Alex";
        Console.WriteLine("Hello " + name + "!");
        //--------------------------------------
        //User Input
        string s = Console.ReadLine(); //For words
        int x = Console.Read(); //For numbers
        //--------------------------------------
        //If statements
        bool condition = true;

        if (condition) {
          Console.WriteLine("The variable is set to true.");
        }
        else {
          Console.WriteLine("The variable is set to false.");
        }
        //--------------------------------------
        //For loop
        for (int i = 1; i < 11; i++) {
          Console.WriteLine(i);
        }  
        //--------------------------------------
        //While loop
        int n = 1;
        while (n < 6){
            Console.WriteLine(n);
            n = n + 1;
        }
      }
    }
}
```
### 6.6 | In Closing

Thank you for sticking with us for the first term of Code Cadets covering programming basics and useful skills involving git and the command line. When you return after the Break we will begin our dive into the Unity Engine.

If you haven't already, please send an email to Mr. Purcell to confirm any class changes you may need as we move forward into the Winter Sports season
