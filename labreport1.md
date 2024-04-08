# Lab Report - 1
April 2, 2024

## cd
- Is used to switch current working directory to given path
- No output if it works

1. no arguments 
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads/lecture1**
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cd```
  - No output. We have been exited out of the current working directory and `pwd` command now only shows ```/Users/adyasachdev```

2. path to a directory as an argument
  - Absolute path to working directory right before command was run: **/Users/adyasachdev**
  - ```adyasachdev@Adyas-MacBook-Air ~ % cd Downloads```
  - No output. The current directory has now been moved to the downloads folder and `pwd` command now shows ```/Users/adyasachdev/Downloads```

3. path to a file as an argument
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads/lecture1**
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cd messages```
  - No output. The current directory has now been moved to messages withing lecture1 and `pwd` command now shows ```/Users/adyasachdev/Downloads/lecture1/messages```
    
---

## ls
- Lists files and folders (contents) in current working directory

1. no arguments 
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads/lecture1**
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % ls
    Hello.class     Hello.java      README          messages```
  - Listed the contents in current directory, lecture1

2. path to a directory as an argument
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads**
  - ```adyasachdev@Adyas-MacBook-Air Downloads % ls lecture1
Hello.class     Hello.java      README          messages```
  - Since we are in Downloads and run the command `ls lecture1` it again lists the contents in the lecture1 directory

3. path to a file as an argument
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads/lecture1**
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % ls messages
en-us.txt       es-mx.txt       hi-in.txt       zh-cn.txt```
  - Since we are in lecture1 and run the command `ls messages` it lists the files in messages

---

## cat
- Prints contents of files

1. no arguments
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads/lecture1**
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cat
```
  - There is an *error* since we did not write any arguments after `cat` to be printed. Hence there are no outputs, instead any command we give to the terminal is echoed. We need exit out of the terminal (control + C for mac) to use it again. 

2. path to a directory as an argument
 - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads**
  - ```adyasachdev@Adyas-MacBook-Air Downloads % cat lecture1
cat: lecture1: Is a directory```
  - There is an *error* since we tried to print the contents of a directory. The path we intend to print must have a printable file or files. 

3. path to a file as an argument
  - Absolute path to working directory right before command was run: **/Users/adyasachdev/Downloads/lecture1/messages**
  - ```adyasachdev@Adyas-MacBook-Air messages % cat en-us.txt
Hello World!```
  - Prints the content within the file in the messages directory.
