# Pondering Paths
## The Root

 "/" this defines our directory (also means root directory) you want open, search or whatever operation we wish to do on it, and /pwn is an example of absolute path

## Program and absolute paths

/challenge = here "/" is the root directory and "challenge" is the directory in which run program is stored which when executed gives us our flag token

## Position thy shelf

cd (change directories) =  shift b/w directories

## Position elsewhere

hacker@dojo:~$ = in this `~` is replaced by the cwd (current working directory) we are in and by cd we shift b/w directories

## Position yet elsewhere

also things defined by "/" is considered an absolute path

## implicit relative paths, from /

anything defined with the first slash is the absolute path and anything after it is relative path. for eg: file is located in /tmp/a/b/file1. Then /tmp --> absolute path and ../a/b/file1 --> relative path

## explicit relative paths, from /

"." refers to files in the same directory. for eg: /challenge or /./challenge (absoluted paths) and challenge or ./challenge or challenge/. (relative paths) are the same thing

## implicit relative path

run command can't be executed directly in the terminal to avoid executing programs in our current directory that happened to have the same names as core system utilities. (basically a saftey measure of sorts)
very confusing at first to make use of implicit paths to find and execute the run command. [i have no idea how i did it, need to go through this again]

## home sweet home

i did /challenge/run ~ and got the output (just for the sake of it, ~ is called tilde)

Writing the file to /home/hacker!
/challenge/run: line 29: /home/hacker: Is a directory
... and reading it back to you:
cat: /home/hacker: Is a directory

now how am i supposed to get the flag from this? should go to challenge directory but that just returns me to the invoke error
cat run is also not helping cant glean much information from it or maybe i missed something??

ok i just didnt read the question clearly or missed what it meant, basically the issue with what i wrote above is that just ending the line at "~" just speicifed the directory but didnt actually write out my flag

i was supposed to do this simply (smh)
> /challenge/run ~/h

> Writing the file to /home/hacker/h!
> ... and reading it back to you:
> pwn.college{0mMe482ivgTb5hIh5dBWPM7vUdX.dNzM4QDL5EzN0czW}
