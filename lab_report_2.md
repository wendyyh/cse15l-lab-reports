# CSE 15L Lab Report 2: Servers and Bugs
## Part 1: Web Server
To write a web server called `StringServer` that keeps track and add a single string to the server's string message by incoming requests of `/add-message?s=<string>`, we need to first create a new java file containing a class `Handler` that implements the interface `URLHandler` and a class `StringServer` to initiate the a new `Handler` object with a certain port number. 

The code for StringServer.java would look like this (I used NumberServer.java from CSE15L lab 2 class activity as a reference source): 

A port number is any number between 1024 to 49151.
