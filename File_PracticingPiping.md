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

# Grepping live output

# Grepping errors

# Duplicating piped data with tee

# Writing to multiple programs

# Split-piping stderr and stdout
