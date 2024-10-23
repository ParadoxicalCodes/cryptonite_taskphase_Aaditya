/etc/psswd stores the list of all users on a linux system

# Becoming root with su
su (switch user) --> allows us to switch user to root user
su has SUID bit hence it runs as root though we need a password to use it

Once the password is entered correctly, the system recognises us as root instead of hacker hence allowing us to read the flag

![image](https://github.com/user-attachments/assets/cc8062e9-3238-4e0c-b43a-94e2d12100d1)


# Other users with su
without argument, su switches to root user (or start a root shell)

By appending a username after su we can switch to that username too

# Cracking Passwords
passwords for users used to be stored in /etc/psswd. Now they are stored in /etc/shadow

![image](https://github.com/user-attachments/assets/7ba8213b-c20b-4e90-8296-e235a87e0509)

this is the contents of /etc/shadow of prev challenge

Each field is seperated by ":"

First field --> Name of the user

Second field --> password (that long strings are hashed)
When a password is input it checks the has and verifies, if correct su works otherwise it doesnt. And * or ! in this field simply means that password/login is disabled for this username, and blank field means no password.

John - this command helps us decrypt the hashed passwords in the event we can access the backup of /etc/shadow which is not protected

![image](https://github.com/user-attachments/assets/29e4b71f-d595-47a4-a82b-6babe23ea97b)


# Using sudo
sudo (superuser do) --> this basically runs a command as root instead of switching to a user like su

## Thought process

> sudo /challenge/run

this just basically read the challenge desc so i did
> sudo /flag

but that just gave an error saying /flag not found
So instead i thought of chaining it witch cat /flag
> sudo cat /flag

and this works!

