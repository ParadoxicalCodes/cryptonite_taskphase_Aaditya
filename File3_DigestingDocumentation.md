# Learning From Documentation

basically we were given an intro nested arguments - argument within an argument
we had this in the find command

> find -name file_name 

everything after find is an argument and within it we have -name and things after it is also argument - so nested arguments

# Learning Complex Usage

## places where i was stuck
### edit 0
i got the correct argument

> /challenge/challenge --printfile /challenge/challenge 

i just need to modify what should be put after --printfile argument slightly confused here?

## edit 1
im stupid i simply had to do thi

> /challenge/challenge --printfile /flag

but i though flag file cant be read catting flag still return permission denied so how are we able to print the flag file??

# Reading Manuals
man =  a command to open manual for a command we dont know
just do man cmd_name we dont have to actually put the directory in which the cmd is just write the cmd name in the argument

# Searching Manuals
after the man command you can sift through the results using "/"
also n = goes to next page
N = goes to prev page of search results

# Searching For Manuals
man man = essentially a manual for the man command itself
from this i found the "-K" argument which would let me find the a man page for the challenge
-k, -apropos = searches the man page for the description or names i put in (a search modifier sort of)

# Helpful Programs
-h = alternative to man cmd

# Help for Builtins
builtin cmds are commands stored in shell rather as an executable program like man or -help
an example of builtin cmd --> help
