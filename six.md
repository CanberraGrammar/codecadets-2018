---

title: Week 6

---

### 6.1 | End of Term

Welcome back once more for the last time this Term. By now you have probably learnt various basic Software skills such as a the Terminal and Git, and are familiar with basic programming techniques.

Today we won't be introducing any new concepts. It's the last week of term, everyone's mind is likely on the holidays ahead. So instead we're going to get you to go over some programming challenges to help improve your ability to read and write C#, so that when we move onto Unity it's more familiar to you.



<font color='red'>You do not have to do these in any particular order, or complete all of them by the end of the session</font>They are here to help you get better at writing C# code. If you get stuck on one feel free to try another.

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

For a list of useful operations and commands, look to the bottom of the page.

### 6.2 | Sequence and Selection challenges

1. **(C# Warmup)** Write a program in C# that asks the user for their `name`, and then responds with `Hello there, name!`. For instance, if I entered `Alex`, it should say `Hello there, Alex!`.

2. **(Easy)** To get you using C# If-statements, write a program that asks the user for an input and returns the following outputs.

  * input = `Hello`; output = `Hello to you too.`

  * input = `Goodbye`; output = `Ok, see you later.`

  * input = `How are you?`; output = `I am well.`

  * For everything else, output `I didn't understand.` You can also add any custom IO pairs you would like.

3. **(Easy)** Write a program that accepts user input for a `mark`, and output a grade accordingly. `(90+ = A; 80-89 = B; 70-79 = C; 60-69 = D; 50-59 = E and less than 50 = F)`.


### 6.3 | Iteration Challenges

1. **(Easy)** Write a program in C# that accepts a user input for a positive number called `n`, and then print all the numbers from starting from `1` up to `n`.

2. **(Easy)** Write a program that accepts a user input for a positive number called `n`, and then print all the numbers from staring from `n` down to `1`.

3. **(Medium)** Write a program that takes user input for `height` and uses loops to output a triangle made of asterisks (with spaces in between each) of that height. E.g, the following pyramid is `height = 5`.



```
*
* *
* * *
* * * *
* * * * *
```
* **(Hard)** For a more difficult challenge, try and make the triangle into a pyramid like so. The following example is also of `height = 5`. Your code should still work for **any possible height**.

```
    *
   * *
  * * *
 * * * *
* * * * *
```


### 6.4 | Putting stuff together

These challenges will require you to use loops **AND** if statements to complete.

1. **(Medium)** Write a `FizzBuzz` program. It prints all numbers from 1 to 100, but every number divisible by 3 is replaced with `Fizz`, every number divisible by 5 is replaced with `Buzz`, and any number divisible by 3 AND 5 is replaced with `FizzBuzz`.

2. **(Medium)** Write a program that loops and asks the user for strings, responding each time with `That's a nice word`, until the user types in `STOP`, where the program will stop asking for input and print `Goodbye`.

3. **(Hard)** Create a program to calculate a student's average mark.

  * It should only accept a valid number from 0 to 100. No more and no less.

  * The program should keep asking the user for a mark until they enter a number outside the range above. For example, when I put in the number `101` it should stop asking me for numbers. Do not record the value of this number.

  * Once the loop asking for input has stopped, calculate the average mark.

  * The formula for an average mark is all the marks added together then divided by the number of marks. For example, let's say I got 80, 72 and 94 on my tests, then `(80 + 72 + 94)/3 = 82` is my average. It's up to you to figure out how to keep track of these numbers during input.

#### If you managed to finish all these challenges, ask your tutor to create some special custom challenge problems for you. These will likely be much harder.


### 6.5 | C# References

Looking for a reminder of what a certain operation looks like in C#? Look no further, here are all the tasks you'd probably want for today's session, but of course, there's always other ways to solve a problem.


```cs
using System;
//A Sample Hello World Program
namespace MyProgram {
   class MyClass {
      static void Main(string[] args) {
          Console.WriteLine("Hello World!");
      }
    }
}
```


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
        else if (!condition){
          Console.WriteLine("The variable is set to false, which is not true.");
        }
        else {
          Console.WriteLine("This is the else if something unexpected happens");
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
