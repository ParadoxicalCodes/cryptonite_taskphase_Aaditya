ls -l  --> this allows us to check the permissions of a file or directory, just append the file/dir after the cmd to check its permissions

![image](https://github.com/user-attachments/assets/f8a12c49-06b2-4d7a-bcac-3e600fad8f3c)

these lines tells us about permissions and file type
first character of the line tells us file type rest 9 characters tell us about permission bits
those 9 are further split into 3groups having 3 bits each, telling us about diff permissions
first 3 bits tell us about permissions of the user that owns the file or owner (root in this case)
next 3 bits tell us about permissions of the groups owning that file
last 3 bits tell us about permissions of the other users/groups

after the permission lines comes two columns shows the users that own the file, in this case hacker-user & hacker-group

# Changing File Ownership
chown -->  this command changes the ownership of the file (generally run by the root user/admin)

Syntax:
> ![image](https://github.com/user-attachments/assets/21ca9f63-9700-471e-8791-2258b0800b4b)

# Groups and Files
id --> this cmd shows what groups we are a part of (no argument needed)
chgrp --> similar to chown but changes the group owning the file (syntax is also similar)

# Fun with Groups Names
Nothing much in this level except after using id cmd it was apparent which gro i was in and appropriately used the chgrp cmd

![image](https://github.com/user-attachments/assets/7f49d52b-8d72-4eaa-85da-14f530d81043)


# Changing Permissions
Continuing the prev discussion on permission

r - represents read access

w - represents write access

x - represents permission to execute

"-" - means nothing i.e no permission

So, something like this "-rwx-r--r--" means:
  - first 3 characters --> root user can read, write and execute the file
  - next 3 --> root group can just read the file
  - last 3 --> other users can also just read the file

chmod - allows us to change the permissions for a file

Syntax by example:
> chmod u+r /flag

this cmd basically added read permission for the root user for /flag

u --> user/owner

g --> group

o --> other user

a --> all users (includes u,g,o)

+/- control the tweaking part i.e. whether to add or remove the permission respectively which is joined by r,w,x and then filename

> chmod og-xr /flag

we can also combine u,g,o & r,x,w to change permissions for multiple users

![image](https://github.com/user-attachments/assets/3c16294d-9b09-49af-b681-b44846870d02)


# Executable Files

![image](https://github.com/user-attachments/assets/b6fa5365-dbc1-4906-bd7b-cf939f05c924)

i first tried to be specific with the cmd but for some reason i couldnt run the file so i tweaked perms for all
Then i tried again to look through which permission actually allows me to run the file

![image](https://github.com/user-attachments/assets/d68b9f5a-324b-4fa4-8643-e24c030358bf)

Turns out it was "u" that allowed me to read the file and changing perms for g or o resulted nothing which makes sense as /flag is only accessible to the owner or u

# Permission Tweaking Practice
This was simply a practice for getting comfortable with chmod and trying various combinations u,g,o and r,w,x in the chmod cmd

# Permissions Setting Practice
Before this we were simply changing the permissions,
Now we can set the permissions which would override previous perms by simply introducing "=" into the syntax
Also we can chain multiple permissions overwrites by seperating with "," and no space around the commas

For example:

>![image](https://github.com/user-attachments/assets/35c659e9-8f19-472f-8dc8-14b2b08d4760)

>![image](https://github.com/user-attachments/assets/4f568632-4656-418e-92ea-563830419bee)

also by doing "=-" or "=+" for any user/group will remove or add all permissions for that user/group

# The SUID Bit

SUID stands for Set User ID --> this permission bit allows the user to run the program as the owner itself

Syntax:
>![image](https://github.com/user-attachments/assets/a31957ae-c025-498b-91a9-cc924e40ede4)
