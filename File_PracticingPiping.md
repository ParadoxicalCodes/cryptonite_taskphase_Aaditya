linux terminal has 3 standard channels of communication
 1. stdin - standard input
 2. stdout - standard output
 3. stderr -  standard error

# Redirecting Output
">" - can redirect outputs to a file
# Redirecting more Output

![image](https://github.com/user-attachments/assets/f6a0fc28-e1c1-4d78-9e55-38375677e640)

~~confused here as to why im getting this output shouldn't i be getting the flag here?~~
i simply had to cat the file for flag

# Appending output
">>" = this lets us append all our output together into one file if the contents are too big
if the contents to be appended are too big then ">" will write one part then overwrite it by 2nd part which we dont want
# Redirecting errors
FD stands for file descriptor  -  its a number that describes a communication channel in linux
FD 0 - stdin
FD 1 - stdout
FD 2 - stderr

by default ">" without a number implies "1>"
now to redirect errors,
```hacker@dojo:~$ /challenge/run 2> errors.log```

this will stderr to errors.log file.

Also one can redirect to multiple files

```hacker@dojo:~$ some_command > output.log 2> errors.log```

# Redirecting input
"<" - redirects inputs to programs

# Grepping stored results
very straightforward from here

```/challenge/run > /tmp/data.txt```

# Grepping live output
"|" - pipe operator - basically removes the middleman (saving output to files) and connects 2 commands directly

# Grepping errors
"|" only redirects our output to fd1, unlike ">" it cant flexibly give our outputs in other fd
">&" - this redirects from a fd to another fd

# Duplicating piped data with tee
tee -  allows us to go through the outputs of our piped cmds for debugging

![image](https://github.com/user-attachments/assets/b6cffc06-e604-4893-befc-4149d7ce4a0b)

### Thought process
```/challenge/pwn | /challenge/college```

i know this is wrong but did this just to get some hints for the challenge from the ouput i receive
 - Above process basically told me i need a secret argument with college to solve it

```/challenge/pwn | tee pwn | /challenge/college```

since i want to intercept the output of first cmd i just wrote pwn but this is wrong, even "tee /pwn" yields the same result. From the syntax of the code i need to write cmd1_output after tee for it to work so where is the output going??

Just to get a hint i did cat pwn and cat chio.py after cd /c* and ls -a (cat trick)

~~i think chio is the secret word? lets verify it~~

this line of thought is not working better to just start over

> [!WARNING]
> Never just do
> ```cmd1 | tee cmd1 | cmd2```
> that will just overwrite the contents of cmd1 we dont want that

ok its better to find out where the output of /challenge/pwn is or else it will just throw errors everywhere
i dont know where the output is so i just decided to create my own output txt but that also doesnt seem to work?

![image](https://github.com/user-attachments/assets/ead39d54-0fa8-4183-bd2e-604dae319d85)

OHHHHHHHHHHHHHHHHHHH i simply had to do cat pwn_output
ok tee doesnt just show results live rather it stores the outputs to whatever destination we define

```/challenge/pwn --secret gevp4ac- | tee pwn_output | /challenge/college```

# Writing to multiple programs
```/challenge/hack | tee /challenge/the | tee /challenge/planet```
this gave us

![image](https://github.com/user-attachments/assets/7c73ac06-c5ed-4772-bab9-8776d3d8aab3)


# Split-piping stderr and stdout