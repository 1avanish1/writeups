#OWASP TOP 10

##COMMAND INJECTION
user controlled input is interpreted as actual commands or parameters.

###TYPES:

SQL Injection: This occurs when user controlled input is passed to SQL queries.
As a result, an attacker can pass in SQL queries to manipulate the outcome of such queries. 

Command Injection: This occurs when user input is passed to system commands.
As a result, an attacker is able to execute arbitrary system commands on application servers.


###methods:
1)Reverse shell
wHAT IS A shell?
Simply put, the shell is a program that takes commands from the keyboard and gives them to the operating system to perform.
EX:
bash-bourne again shell
others: ksh, tcsh and zsh

a shell script is a file containing a series of commands
