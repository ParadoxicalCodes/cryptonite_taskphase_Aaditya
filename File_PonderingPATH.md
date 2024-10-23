# The PATH variable
PATH --> this is a shell variable that stores directory paths which shell peruses to run commands (kind of like a library for cmds)

![image](https://github.com/user-attachments/assets/ccd468bc-e606-458f-ad62-859ee1b2c078)

>Doubt - revisit later
>While solving this i was slightly confused that if i do PATH="" would remove everything then how would /challenge/run run? is it not possible to specifically remove rm from PATH?

also echo $PATH allows us to look into what dirs are there already

# Setting PATH
![image](https://github.com/user-attachments/assets/f5ba7bfe-1a7c-410a-9b2e-ee8c3ea2eae2)

this is how you put a dir for a cmd to run (but as we can other dirs are gone isnt that an issue?)

# Adding commands
ok i tried the first option of given three

found where cat command is stored (its in /bin) and kept that while changing the PATH variable

the issue was arising when i did everything still didnt get flag. Then i realised the permissions werent there for win hence the errors

![image](https://github.com/user-attachments/assets/8fbad911-6e7a-48e1-a0e8-1ce7c543c98e)


# Hijacking commands
## Thought Process
### try1
found where rm is (in /bin) saw its permissions and tried changing it to just read for all users

![image](https://github.com/user-attachments/assets/b46c8782-d266-44fc-bee3-a502f5f788ca)

### try2
what if i did  rm rm

does that work??   ---> answer is yes it would but we dont have the permissions, what if we tried to get the said permission? (actually this is not possible too the whole operation is denied)

> ![image](https://github.com/user-attachments/assets/46451310-b61d-429c-b03f-762baabddd05)
 
### try3
what if we create a blank rm of our own and remove the directory containing the actual rm and then do /challenge/run   ?

> that wont work because although we saved the flag from getting deleted it still cant be printed out

ok i understood something - the system goes through dirs in PATH in order so what if i put my rm before the actual one then run it?

