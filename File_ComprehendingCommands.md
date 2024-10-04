# cat: not the pet, but command!

cat (concatenate) =  this basically reads out the content of whatever file we specify
i.e. cat <file>

# catting absolute paths

one can put multiple arguments to write out the path of our file where ever it is
another thing to note = cat can read out multiple files at once

# more catting practice

since we didnt know where the flag was located i wrote "cd /" so i could get correct directory of the flag instead of chasing it around

# grepping for a needle in a haystack

grep is like cat but more specific and is mainly used when the file we are reading has a lot of lines

![img1](https://github.com/user-attachments/assets/c06fac02-4a84-4270-8c40-4174267473da)

# listing files

ls = lists all the contents of a file or directory

# touching files

touch = command to create files

# removing files

rm = command to remove files

# hidden files

files that start "." are hidden, for them to show up just do "ls -a" to show all files including the hidden ones in whatever directory you are in

![im2](https://github.com/user-attachments/assets/e2ad0dac-1add-4a25-83b0-d85cb6e321db)

# An epic filesystem quest

with the combination of commands cd, ls and cat im supposed to find a file hidden in some directory. i have reached the trapped hint part but how am i supposed to open it without destructing it? 
> lets just try that cat trick first
> the run file is not there, well ofc it wont be there so its most likely saved in that fuc directory as run what if i execute it without going into just fuc so as to avoid the too many arguments error?
> 
> ![img23](https://github.com/user-attachments/assets/f1836384-24fb-4f75-8325-cdc88bc2bbe4)
>
> i went two directories back that also didnt work should i just stay in / rather than cd ing into /opt ??

got it got it now 
![image](https://github.com/user-attachments/assets/61c03967-dd91-49a4-9be8-7582f98718e0)

rest was easy to follow

# making directories

mkdir = command to create directories
> made a mistake of doing mkdir college instead of touch college
> mkdir will ONLY creat directories not files (to keep in mind!)

# finding files

find = cmd to find directories or files
"-name" is a filter to narrow our search, if we leave "find" as is it will return **all** matching results

> ![image](https://github.com/user-attachments/assets/6e2d1ada-c7e0-4e1d-9cd3-5a45807dc73f)

> why is the flag token behind the shell prompt? why is the output like that?
> and is not possible to find by using a filter that distinguishes between a file and directory?

# linking files

