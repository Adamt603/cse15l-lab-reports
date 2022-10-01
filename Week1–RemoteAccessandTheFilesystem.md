#  Week 1 - Access and the Filesystem

In this project we discuss how to download and setup VS code, remotely connect to ieng6 using ssh, run various commands, copying files over ssh, and generating ssh keys.

---
## How to install Visual Studio Code


### Step One 
![Vs code download](https://github.com/Adamt603/cse15l-lab-reports/blob/main/Imagies/firstPic.png?raw=true)
- Go to [VS code download](https://code.visualstudio.com/) and click "Download Mac Universal"  
- Then go through all the prompts and finish installing the IDE.
- Open it once the installation is complete and look for a tab at the top that says Terminal then click open new terminal. 
- The terminal is where you will type all your git commands and ssh commands.

---

## How to remotely connect 

### Step Two
![Remote SSH into ieng6 server](https://github.com/Adamt603/cse15l-lab-reports/blob/main/Imagies/Second%20pic.png?raw=true)
- Open up Visual Studio Code and then open up a new terminal.
- Type "ssh cs15lfa22ii@ieng6.ucsd.edu" for me it is ii for you it will be something different. 
- You will be prompted to type in your password, type it in.
![Finally logged on](https://github.com/Adamt603/cse15l-lab-reports/blob/main/Imagies/Thrid%20pic.png?raw=true)
- Now you are logged into the ieng6 remote server, where your code will be executed and your files will be stored. 



---

## How to moving files with scp
### Step Three
- Next on your remote computer you will want to open the terminal and type scp fileName.extensionType severAddress:Directory
- This will copy the file from your remote machine to the server.
- When done you can remote SSH into the server to check to see if the file is in the directory you sent it to.
![](https://github.com/Adamt603/cse15l-lab-reports/blob/main/Imagies/Fourth%20image.png?raw=true)
---

## How to set up an SSH key
### Step Four 

---

## How to optimizing remote running
### Step Five

---

### **Back to main page**
  - [**Main page**](https://adamt603.github.io/cse15l-lab-reports/)



