# CSE 15L Lab Report 4: Command Line Tasks
This lab report will demonstrate the process of completing the command line tasks from [CSE 15L week 7 lab](https://ucsd-cse15l-s23.github.io/week/week7/#lab-tasks---doing-it-all-from-the-command-line) with the repository [lab7](https://github.com/ucsd-cse15l-s23/lab7) (fork it before starting all tasks) in the terminal.

## Log into ieng6
The first step is to use command `ssh` to log into our course specific ieng6 account. The keys pressed are:
`ssh<blank><ieng6 course specific account><enter>`. Then type in the password (note that the keys pressed at this phase stay invisible for privacy): `<password><enter>`.
After successful log-in, the output would be like this:
![ieng6 login page]()

## Clone your fork of the repository from your Github account
In this step, we are going to clone the fork of the repository [lab7](https://github.com/ucsd-cse15l-s23/lab7) from our own Github account. Use the url from our own fork of the repository for `git clone`. The keys pressed are: `git<blank>clone<fork repo url><enter>`. After a successful cloning of fork, the output would be like this:
![git clone page]()

## Run the tests, demonstrating that they fail
To run the tests, we need to firsh change current directory to lab7 in our remote server. The keys pressed are: `cd<black>lab7<enter>`. Then we can use key `ls<enter>` to check the files/directories in `/lab7`. The output is:
![cd and ls page]()
We see that there is a `test.sh` file that we can use the `bash` command to run a series of commands that has been already given in the file to test the code. Then we can press keys `bash<blank>test.sh<enter>` to run the tests for the java file `ListExamples.java`. The output demonstrates that there is 1 failure of 2 tests from `ListExamplesTests.java`:
![bash test.sh page]()

## Edit the code file to fix the failing test
In this step, we need to edit `ListExamples.java` to fix the failing test. We have been informed that the error in the code is just that index1 is used instead of index2 in the final loop in merge.

## Run the tests, demonstrating that they now succeed

## Commit and push the resulting change to your Github account
