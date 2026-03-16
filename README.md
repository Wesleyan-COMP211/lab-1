# Lab 1: Setting up and checking your development environment

The goal of this lab exercise is to get a bit of practice using the shell (command-line environment) and a plain text editor, and to write a very simple C program, compile it, and execute it.  

To get a shell in Windows, use the Power Shell application, and type

```
> wsl
```

(without the `>`). 

To get a shell in MacOS, use the Terminal application.  

## Learning about the command line

You should have already viewed the YouTube video in the [development environment document](https://docs.google.com/document/d/1a-7eR9yxayGPi1gIJrx-ekz0FrLfJ_sENim8SsJbwQA/edit?usp=sharing) about using the command line. 

## Make some directories

Using shell commands, change to the directory in which you will keep all your files for COMP 211.

For example, if the directory is named `comp211` and it is in your home directory, and the current working directory for your shell is your home directory, then

```
$ cd comp211 
```

Make a `labs` directory, and in that a `lab1` directory:

```
$ mkdir labs
$ cd labs
$ mkdir lab1
$ cd lab1
```

## Edit a file

Download the `lab1sample.txt` file that is posted for this lab into your `lab1` directory. Copy the file to `lab1stuff.txt` using the `cp` command, which is invoked as

```
$ cp file1 file2
```

to copy `file1` to `file2` (use the actual filenames, of course). 

Use your plain text editor to edit `lab1stuff.txt` according to the instructions in the file. 

## Write, compile, and execute a program

Use your editor to create a file in `lab1` whose contents are exactly those of Program 1 (below). Name the file `hello.c`. Do not copy-and-paste from this file.  Type each character.  Make sure to change `<Your name here>!` to your name.

Program 1:
```
/* COMP 211 Lab 1: Hello World
* <Your name here>!
*/

#include <stdio.h>

int main(void) {
  printf("Hello world\n");
  return 0;
}
```

Compile your program with 

```
$ cc hello.c
```

Execute your program with 

```
$ ./a.out
```

Note that the `./` part is required. It tells the shell to look for a program `a.out` in the current directory. If you try to execute your program with 

```
$ a.out
```

you will get an error to the effect that there is no such program -- try it!

Remove `a.out` with the `rm` command: 

```
$ rm a.out
```

Re-compile your program with 

```
$ cc -o hello hello.c
```

The option `-o hello` tells the program cc which is compiling your code to name the output file (the executable) `hello` instead of the default name, which is `a.out`. Execute your program by telling the shell to run `hello` instead of `a.out`. 

## Upload your files to the GitHub repository

Go to your repository through the web interface in your browser. You should see a big green button that says "<> Code" towards the top of the page. 

To the left of the big green button, there should be a grey "Add file" button. Click on this button and select "Upload files".

Upload your `hello.c` file, either by dragging and dropping or by using the "choose your files" dialog. Do not upload your executable (the `hello` file with no extension). 

Repeat this process with your `lab1stuff.txt` file. 

Click the green "Commit changes" button. 

## Check that your file is uploaded correctly

Go back to your repository's main page. 

You should now see your `hello.c` file listed along with `README.md` and `lab1sample.txt`.

The `lab1sample.txt` file should have been updated, but not replaced. 

Click on the `hello.c` file. You should see the code that you wrote. 

Go back to the main page. 

Click on the `lab1stuff.txt` file. You should see the text that you added to the file instead of the original file. 

You can use this procedure to check that files are successfully uploaded to the repository whenever you turn in your assignments. 

That's it!! You're done!
