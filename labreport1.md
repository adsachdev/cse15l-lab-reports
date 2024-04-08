# Lab Report - 1
April 2, 2024

## cd
- Is used to switch current working directory to given path
- No output if it works

1. no arguments 
  - Absolute path to working directory right before command was run: /Users/adyasachdev/Downloads/lecture1
  - ```adyasachdev@Adyas-MacBook-Air lecture1 % cd```
  - No output. We have been exited out of the current working directory and `pwd` command now only shows ```/Users/adyasachdev```

2. path to a directory as an argument
  - absolute path to working directory right before command was run: /Users/adyasachdev
  - ```adyasachdev@Adyas-MacBook-Air ~ % cd Downloads```
  - No output. The current directory has now been moved to the downloads folder and `pwd` command now shows ```/Users/adyasachdev/Downloads```

3. path to a file as an argument
  - absolute path to working directory right before command was run: /Users/adyasachdev/Downloads/lecture1
  - ```adyasachdev@Adyas-MacBook-Air ~ % cd messages```
  - No output. The current directory has now been moved to messages withing lecture1 and `pwd` command now shows ```/Users/adyasachdev/Downloads/lecture1/messages```
---

## ls
- Lists files and folders (contents) in current working directory

