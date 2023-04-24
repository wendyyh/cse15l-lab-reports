# CSE 15L Lab Report 2: Servers and Bugs
## Part 1: Web Server
To build a web server called `StringServer` that keeps track and add a single string to the server's string message by incoming requests of `/add-message?s=<string>`, we need to first create a new java file containing a class `Handler` that implements the interface `URLHandler` and a class `StringServer` to initiate the a new `Handler` object with a certain port number. 

The code for **StringServer.java** would look like this (I used NumberServer.java from CSE15L lab 2 class activity as a reference source): 
![StringServer code](lab2_StringServer_code.png)

To run the server on a local computer, we may use the following commands from the current directory of the clone of the repository in the terminal:
```
javac Server.java StringServer.java 
java StringServer 4000
```
(Note that 4000 is a random port number that you may replace. A port number is any number between 1024 to 49151.)

If both commands run successfully, it would provide a link of the server for you to visit and put in requests.
![run commands](lab2_run_server_commands.png)

To access the server, open the link it provides in a browser and add the add-message requests to the end.
