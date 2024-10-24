# Printing Variables
we can print out variables too by just prepending the variable with "$"

# Setting Variables
values can be stored into variables using "=" with no spaces around it otherwise the shell will just read the first word as some cmd and run it

for example:
> VAR=20
> echo $VAR

the output will be "20"

# Multi-word variables
in order to store more than just one term to a variable, encase the terms inside " "

for example:
> VAR="20 food"

# Exporting Variables
sh - a cmd that opens a child of the main shell 

by default, variables set are local to that shell and wont carry over to other shells

export - cmd to export over variables to the child shell allowing us to circumvent the default setting

## Thought process
> ![image](https://github.com/user-attachments/assets/410cba6a-85a7-4514-95c9-623cd13728f7)


# Printing exported variables
env - prints out every exported variable set in the shell

env is kind of like echo but just for exported variables

# Storing command output
cmd outputs can be stored into a variable with the help of "&()"
>syntax
>
>![image](https://github.com/user-attachments/assets/50d3677a-5ace-4ae3-92cd-00a58323671a)


backticks "``" can also be used for the same purpose but it will make it difficult if we ever nest our commands

![image](https://github.com/user-attachments/assets/d3bc5f96-8aa3-44b1-b9b6-ffbcd296b020)


# Reading input
read - cmd that allows us to get input from the user
" -p" this argument allows us to specify a prompt

also the difference b/w read and echo is that former shows the input while echo shows the output
![image](https://github.com/user-attachments/assets/0bb96e42-e77e-4db3-8c80-fe9ae66c33f8)

And,
![image](https://github.com/user-attachments/assets/8cfda94b-f177-49a8-8f99-8024bf8a54a5)


# Reading files
using "read" we can read files

>![image](https://github.com/user-attachments/assets/a5a5572f-3bb2-47d5-91bc-315c5f2d33a0)

some_file redirects into stdin of read, read then reads into VAR which then reads the file


![image](https://github.com/user-attachments/assets/d3ca9369-332c-4b76-b7a4-59b4e714f443)
