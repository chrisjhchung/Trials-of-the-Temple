# May the Force be with You

## Instructions

This is the first exercise. The goal is to print "May the force be with you" to the console. You will need to learn how to use the `printf` command. For more information, you may run:

```
man printf
```

to see the manual. To start, open `mayTheForceBeWithYou.c` and implement the code under:

```c
// your code goes here
```

## Compiling and testing

To compile, simply run `make`. To test, simply run `make test`.

## Advanced

Note this section requires GCC to be installed on your machine. It should already be there if you're using a UNIX machine (Mac or Linux). If you're using Windows, please follow this guide:
https://gcc.gnu.org/install/binaries.html

If you want to learn more about compilation, try compiling the code yourself, without the makefile. To do this, we will use `gcc`. You can use the following command to turn your code into an exectuable, which your machine can run:

```
gcc mayTheForceBeWithYou.c
```

This will result in a file called `a.out`/`a.exe` (Depending on your OS), which you can then run by using `./a.out`/`./a.exe`. Additionally, if you want to rename this exectuable you can run:

```
gcc mayTheForceBeWithYou.c -0 <YOUR-DESIRED-NAME-HERE>
```

and then you can run it by running: `./<YOUR-DESIRED-NAME-HERE`