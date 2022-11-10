# Week 7 Part 1: Using vim

---

## In DocSearchServer.java, change the name of the start parameter of getFiles, and all of its uses, to instead be called base.

```vim DocSearchServer.java```
- opens DocSearchServer.java in vim
```:%s/start/base<Enter>:w```
- Find each occurrence of 'base' (in all lines), and replace it with 'start'.
- ![Show changes](Imagies/week7lab/Screenshot%202022-11-10%20at%201.17.09%20PM.png)
- This image shows the changes after executing the command.

--- 

# Week 7 Part 2: bash

VSCODE time
- 2 minutes
vim time
- 27 seconds

## Which of these two styles would you prefer using if you had to work on a program that you were running remotely, and why?

- If a small change needed to be done vim makes more sense. But if I'm programming something massive I prefer VScode especially when working remotely, because if the schools internet has anything to say about it then I'm not coding most of my time is spent trying to reconnect to that remote server. 

## What about the project or task might factor into your decision one way or another? (If nothing would affect your decision, say so and why!)
- Another thing that would factor into my decision would be if I needed a more powerful PC to run my code or even a different operating system. For example, In CSE30 we need a 32-bit machine and my personal computer is 64-bits.
