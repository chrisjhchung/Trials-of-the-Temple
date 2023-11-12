# May the Force be with You

## Instructions

This exercise will teach you a basic understanding of "variables", "types" and also introduce you to a new function, `sprintf()`.

The goal of this exercise is to create a script that reads in a name of a hero, which we can call for help from. For example, a working script will look something like:

```bash
$ Insert name: ObiWan
$ Help me, ObiWan! You're my only hope!
```

Note, `Insert name: ` here is actually an input. `ObiWan` was the value that was inputted by the user. To achieve this, have a look at the `sprintf()` function's documentation. 

https://linux.die.net/man/3/sprintf

### Variables

If you're familiar with maths, you might recognise the idea of variables. For example, you might have:

```
19x + 5 = 100
```

Where `x = 19`. Of course, if you changed the value on the right, the value of `x` would change too. The idea is that `x` is just a placeholder. This is also true in programming. We can assign values to variables. This can be especially handy if that value is expected to change. 

A good example of this is if we extended the previous chapter's code. Let's say we wanted to write "May the force be with you, Luke". We could easily achieve this by doing:

```c
printf("May the force be with you, Luke");
```

But what if we now wanted to say Leia? What about Yoda? It would be quite tedious having to change that line, every time we want to make a change. Instead, we can store the name of the person into a variable, and then print that variable. That way, no matter who we are saying may the force be with you to, the print statement will never change:

```c
char[] name = "Luke"; // this can be changed to whatever you want
printf("May the force be with you, %s", name); 
```

Now, the print statement will replace `%s` with whatever the value of `name` is. In the above example, that would be "Luke". This is obviously a small example, but you can imagine, if we had a big codebase where we're printing Luke's name in 100 places, it would be a pain to have to change it in each place. It's much simpler if we referenced the `name` variable in each spot, that way we only need to change the code in one place. 

At this point, you're probably wondering what that funky looking `char[]` and `%s` things are. That's where we learn about types. 

### Types

C (And many other languages) rely on types. You're probably wondering what types are. Types tell a machine what kind of variable something is. Here are a few examples of types available to be used in C:

```
int --> Used for whole numbers
double --> Used for numbers with decimal places
char --> Used for single characters
char[] --> Used for a list of characters, or "strings"
```

This list isn't exhaustive, but it should be enough for now, and should also get you thinking about the different types of types. This concept is important, since understanding types will help you debug your code. 

You can perform mathematical formulas on number based types (like `int` and `double`). For example:

```c
int a = 5;
int b = 10;
int c = a + b; // c = 15
```

But you can't perform maths on a string

```c
int a = 5;
char b = "10";
int c = a + b; // this will fail
```

## I/O

I/O, or input and output describes the methods for inputting and outputting data to code. For this exercise, we will need a way to prompt the user for an input, then read that input, then store that input in a variable, which we will then use later. 

Have a look at the `sprintf()` function, it behaves very similarily to the `printf()` function. Except, instead of printing out to the console, it reads data from the console. 

## Compiling and testing

To compile, simply run `make`. To test, simply run `make test`.
