# Matching with *
"*" when put in an argument acts as a wildcard (or empty slot which is filled with all possible combinations allowed by dir or command it is in)

note - you can do something like this cd /c*/f* but /*/f*  wont cd us into /challenge/files
# Matching with ?
"?" works the same as "*" but for a single character. The latter fills as many empty places as possible while former does it for just one place
# Mathcing with []
again "[]" similar  "?" but it looks for characters in word inside the brackets individually

![image](https://github.com/user-attachments/assets/c89ecf26-3525-4be9-b0c8-e92b61c2ffe1)

# Matching paths with []
"globbing happens on a path basis" - this means that commands happen on the path given rather than doing it on the whole directory (unless specified by this "/")
# Mixing Globs

![image](https://github.com/user-attachments/assets/cf6d4cfd-abc0-40b0-a68e-77b6b27b256b)

the thought process here was very erratic i was basically trying different mixed globbing commands. After this i reread the challenge description and got the correct command
# Exclusionary Globbing
[] - this can also help us filter our globbing
   - putting "!" or "^" before the globbing input will basically give results not having the globbing input

![image](https://github.com/user-attachments/assets/5662ff8f-02ff-4ad6-9de5-aeb45abc882f)

as for my thought process pretty close with the required commands was just missing a "*"

![image](https://github.com/user-attachments/assets/c373fc51-287a-47b2-8073-c997209a20de)

