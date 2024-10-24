# Chaining with semicolons
apart from piping we can also chain commands by joining them with ";"

For example:
> echo COLLEGE > pwn
> cat pwn

above is same as
> echo COLLEGE > pwn; cat pwn

# Your first shell script
i got confused on how to write a shell script, after a bit of tinkering around i got it

> touch x.sh
> echo "echo "/challenge/pwn; /challenge/college" >> x.sh
> bash x.sh

here i basically put my commands as a string and appended it to x.sh then ran it in shell to get the flag

# Redirecting Script output
i was making a mistake by doing this
> bash x.sh > /challenge/solve

turns out i was supposed to do this
> bash x.sh | /challenge/solve

the mistake was not taking the output as the input for my next command hence i was stuck for a while

# Executable shell scripts
## Thought process
> echo "/challenge/solve" >> a.sh
> ls -l
> chmod a=rwx a.sh
> ls -l
> ./a.sh

the above steps gave me the flag

did ls -l in between to know if my permissions changed or not, after confirming everything i ran my script
