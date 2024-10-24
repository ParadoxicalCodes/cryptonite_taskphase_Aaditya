# Listing Processes
ps --> shows a list of processes running in the terminal at the moment the cmd was executed

>ps or process snapshot or process status
> we cant just use ps or else it will show "bash" and "ps" as the processes, hence some arguments are needed

ps aux --> 'a' lists processes for all users, 'x' lists processes not running in terminal, 'u' gives output in "user readable format"

ps -ef --> "-e" simply shows every process running and "f" gives output in 'full format'

![image](https://github.com/user-attachments/assets/b493b74e-2520-44f4-af8d-c0cacd4ae2ac)

PID - Process ID, its a numerical identifier for each process

TIME - shows total utilised CPU time

# Killing Processes
kill --> terminates a process in a way where it lets the process do proper procedure before terminating it

kill (PID_of_the_process_to_kill)  --> this is the format

# Interrupting Processes
Ctrl-C --> allows us to interrupt/stop any current process runnning or waiting on the input from terminal

# Suspending Processes
Ctrl-Z --> allows us to suspend the current running process instead of directly shutting it off

![image](https://github.com/user-attachments/assets/02844851-75a1-4ac8-9271-3cf72854d50a)


# Resuming Processes
fg --> allows us to resume the suspended process in foregorund (reverse of Ctrl-Z) (no argument needed for this cmd for now)

# Backgrounding Processes
bg --> does the same as fg but resumes process in background which frees up the terminal while running another process simultaneously

![image](https://github.com/user-attachments/assets/a9b755f1-d0d6-4f99-8933-af10a669c3f0)

Under the STAT columns
S --> means the process is sleeping and since there is no "+" after it means its running in background

T --> means the process is suspended

R+ ---> means the process is actively running in the foreground

# Foregrounding Processes
you can bring forward a process from background to foreground by "fg" just as how its done for suspended processes

# Starting Backgrounded Processes
By appending "&" after the command we can directly run the process in background instead of suspending it first then bg

# Process Exit codes
"?" --> allows us to know the exit codes of a process, needs to be prepended with $ as its a variable
0 means code executed as it was intended
1 (or nonzero value) means code didnt execute properly and there were some errors
