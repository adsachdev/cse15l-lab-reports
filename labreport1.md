# Lab Report - 1
April 2, 2024

## cd
- Is used to switch current working directory to given path
- No output if it works

1. no arguments 
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads/lecture1`
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cd```
  - No output and _no error_ is seen. We have been exited out of the current working directory and `pwd` command now only shows ```/Users/adyasachdev```

2. path to a directory as an argument
  - Absolute path to working directory right before command was run: `/Users/adyasachdev`
  - ```adyasachdev@Adyas-MacBook-Air ~ % cd Downloads```
  - No output and _no error_ is seen. The current directory has now been moved to the `Downloads` folder on my laptop and `pwd` command now shows `/Users/adyasachdev/Downloads`

3. path to a file as an argument
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads/lecture1/messages`
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cd es-mx.txt
    cd: not a directory: es-mx.txt```
  - An _error_ with the error message `cd: not a directory: es-mx.txt`. Since `cd` only allows us to change *directories* and hence we cannot enter into files.
    
---

## ls
- Lists files and folders (contents) in current working directory

1. no arguments 
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads/lecture1`
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % ls
    Hello.class  Hello.java  README  messages```
  - _No error_, listed the contents in current directory we are in, `lecture1`

2. path to a directory as an argument
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads`
  - ```adyasachdev@Adyas-MacBook-Air Downloads % ls lecture1
    Hello.class     Hello.java      README          messages```
  - _No error_, and since we are in `Downloads` and run the command `ls lecture1` it again lists the contents within the `lecture1` directory

3. path to a file as an argument
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads/lecture1/messages`
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % ls es-mx.txt
    es-mx.txt```
  - _No error_, and the terminal just prints out the name of the filename itself, in this case `es-mx.txt`

---

## cat
- Prints contents of files

1. no arguments
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads/lecture1`
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cat
        ```
  - There is _no error_ since this command is allowed. However, there are no outputs, instead anything we type in the terminal is echoed (reads data from standard input and writes it to its standard output). We need to exit out of the terminal (control + C for mac) to use it again. 

2. path to a directory as an argument
 - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads`
 - ```adyasachdev@Adyas-MacBook-Air Downloads % cat lecture1
    cat: lecture1: Is a directory```
  - There is an _error_ since we tried to print the contents of a directory. The path we intend to print must have a printable file or files. 

3. path to a file as an argument
  - Absolute path to working directory right before command was run: `/Users/adyasachdev/Downloads/lecture1/messages`
  - ```adyasachdev@Adyas-MacBook-Air messages % cat en-us.txt
    Hello World!```
  - Prints the content within the specified file `en-us.txt` in the `messages` directory.
