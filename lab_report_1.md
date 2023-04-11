# CSE 15L Lab Report 1
## Installing VScode
(If you choose to use a computer in the lab, you may skip the installation and simply open Visual Studio Code on a lab computer.) 

**Visual Studio Code** is a code editor we will be used in future CSE15L labs. Go to [VS Code Website](https://code.visualstudio.com/) and follow the instruction on the website. Choose the version that is right for your operating systems (i.e macOS for Macs, Windows for PCs). Follow steps in the downloaded package to install VS Code on your computer.

After installing the VS Code successfully on your computer, you are now able to open it and should see a window like this:

![VS Code Screenshot](lab1_vscode_sc.png)

Now you are ready to connect your own device to the remote server!

## Remotely Connecting
(If you use a Windows system, install `git` on [Git for Windows](https://gitforwindows.org/). After installation, follow this [Instruction](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) to set up your VS Code terminal with `git bash`.)

Look up and set new password for your student account for the course CSE 15L with Username and Student ID through [UCSD Educational Technology Services](https://sdacs.ucsd.edu/~icc/index.php). Follow this [tutorial](https://docs.google.com/document/d/1hs7CyQeh-MdUfM9uv99i8tqfneos6Y8bDU0uhn1wqho/edit) if you get stucked.

Open a terminal by clicking `Terminal` -> `New Terminal` in the menu bar to utilize `ssh`. Type in a command in this format(replace `<account>` with your specific course account):
```
$ ssh <account>@ieng6.ucsd.edu
```
If it is your first time connecting to this remote server, you will get a message asking for your intent to continue connecting. Type in `yes`, press enter, and type in your account password to continue. Otherwise, you only need to type in your password. (The password stays invisible when you type.) Once you log into the remote server successfully, which means the connection from your own device to the remote server completes, you will see something like this in your VS Code terminal:

![Terminal Screenshoot 1](lab1_terminal_sc1.png)

Now you are ready to try out some commands!

## Trying Commands 
Feel free to try different commands you have learned from Week 1 lectures. Either type in commands directly to run code on your computer or type commands after ssh-ing to run code on the remote server. 

Command list to try:
- `cd ~`
- `cd`
- `ls -lat`
- `ls -a`
- `ls <directory>` (replace `<directory>` with `/home/linux/ieng6/cs15lsp23/<account>`, where `<account>` is your course specific account)
-  `cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/`
-  `cat /home/linux/ieng6/cs15lsp23/public/hello.txt`

The screenshot below shows outputs regarding these useful commands. Try it on your VS Code terminal to see if you get similar ones: 
