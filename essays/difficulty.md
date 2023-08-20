---
layout: essay
type: essay
title: "File Descriptor Essay"
# All dates must be YYYY-MM-DD format!
date: 2022-12-11
published: true
labels:
  - Information Technology
---


*File Descriptor Essay.*

File descriptors in the simplest terms can be described as a number that uniquely identifies an open file in a computer's operating system. It describes a data resource, and how that resource may be accessed. When a process makes a successful request to open a file, the kernel returns a file descriptor which points to an entry in the kernel's global file table. The file table entry contains information such as the inode of the file, byte offset, and the access restrictions for that data stream (read-only, write-only, etc.). You can manipulate and change the default behavior of basic file descriptors by leveraging redirection and pipelines. 

 

Commands and scripts in a shell can generate two basic types of outputs: 

STDOUT: The normal output from a command/script (file descriptor 1) 

STDERR: The error output from a command/script (file descriptor 2) 

By default, STDOUT and STDERR are sent to your terminal's screen. In terms of input, STDIN by default reads input from the keyboard (file descriptor). There are multiple ways to redirect output from shell scripts and commands such as redirecting stdout or stderr, or send then to the same file. 

 

A pipe is a form of redirection (transfer of standard output to some other destination) that is used in Linux and other Unix-like operating systems to send the output of one command/program/process to another command/program/process for further processing. Pipe is used to combine two or more commands, and in this, the output of one command acts as input to another command, and this command’s output may act as input to the next command and so on. It can also be visualized as a temporary connection between two or more commands/ programs/ processes. The command line programs that do the further processing are referred to as filters.  The difference between a pipe and a redirect is that while a pipe passes standard output as standard input to another command, a redirect sends a output to a file or reads a file as standard input to a command. 

grep is very often used as a "filter" with other commands. It allows you to filter out useless information from the output of commands. To use grep as a filter, you must pipe the output of the command through grep. 

 

User-defined variables are variables which can be created by the user and exist in the session. This means that no one can access user-defined variables that have been set by another user, and when the session is closed these variables expire. However, these variables can be shared between several queries and stored programs.  
Environment variables are a set of dynamic named values that can affect the way running processes will behave on a computer. The variables can be used both in scripts and on the command line. Environment variables makes it easy when certain standard directories and parameters need to be referenced but where the actual locations or names can vary from computer to computer. 

 

The shell alias is simply a way to reference another command. It can be used to avoid repetitive long typing of commands and shell lines and simplify work or to even make things safer or dumb-proof. You can check if a certain command is actually an alias with the type command. For example, in Ubuntu, ls is actually an alias to show you colorful output. Aliases allow you to shorten commands which will allow a user to quickly complete tasks. 

The while command in Linux is used to repeatedly execute a set of command as long as the COMMAND returns true. The test command is given and all other commands are executed till the given command’s result satisfies, when the command’s result become false, the control will be out from the while command. The syntax is while COMMANDS; do COMMANDS; done. 

 

In Linux and Unix based systems environment variables are a set of dynamic named values, stored within the system that are used by applications launched in shells or subshells. In simple words, an environment variable is a variable with a name and an associated value. 

Environment variables allow you to customize how the system works and the behavior of the applications on the system. For example, the environment variable can store information about the default text editor or browser, the path to executable files, or the system locale and keyboard layout settings. Environment variables are variables that are available system-wide and are inherited by all spawned child processes and shells.  

 

 

The echo command in linux is used to display line of text/string that are passed as an argument . This is a built in command that is mostly used in shell scripts and batch files to output status text to the screen or a file. The syntax is : echo [option] [string] 

When learning shell scripting this is the first command you will learn about to print something in your terminal. echo will print the output to stdout or you can also redirect the output to files. There are two versions of echo. One is bash built in and the second one is an external command. 

 

Bash conditional statements are those which allow us to take some action towards various conditions. These statements implement blocks of code, based on whether the condition specified by the programmer evaluates to true or false. If it evaluates to true, executes a specific block of code otherwise move to the next condition. There are various types of conditional statements in Bash: 

if statement 

if-else statement 

if..elif..else statement 

The “if’ keyword is followed by the condition you want to check. If the first condition evaluates to false, it will then use “elif” condition. If none of the above conditions evaluates to true, it will move to the “else” condition. 

 

Case statement in bash scripts is used when a decision has to be made against multiple choices. In other words, it is useful when an expression has the possibility to have multiple values. This methodology can be seen as a replacement for multiple if-statements in a script. Case statement has an edge over if-statements because it improves the readability of our code and they are easier to be maintained. Case statements in a Bash script are quite similar to Case statements in C language. But unlike C, Bash Case statement stops continuing the search as soon as the match occurs. In simple words, they don’t require any break statement that is mandatory to be used in C to stop searching for a pattern further.   

The full syntax will look something like this: 

case EXPRESSION in 
  Pattern_Case_1) 
   STATEMENTS 
   ;; 
 Pattern_Case_1) 
   STATEMENTS 
   ;; 
 Pattern_Case_N) 
   STATEMENTS 
   ;; 
 *) 
   STATEMENTS 
   ;; 
esac
