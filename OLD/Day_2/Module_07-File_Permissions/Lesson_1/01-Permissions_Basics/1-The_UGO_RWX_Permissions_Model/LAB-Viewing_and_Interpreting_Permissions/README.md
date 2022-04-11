# PERMISSION BASICS
## The User/Group/Other and Read/Write/Execute Permissions Model

## TRY IT - Viewing and Interpreting Permissions

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ls -ld /bin/  ~/  /root/  `
- > Note the ownership and permissions for the directories */bin/*, */home/student/*, and */root/*.
    - > Users without the **execute** permission on a directory cannot `cd` to that location.
    - > The **execute** permission is also required for the **read** and **write** permissions to work properly in a directory.
3. `cd /root `
- > Notice the error message.
4. `cd /bin ; pwd `
- > The **student** user is neither the **root** user nor are they a member of the group **root**, so they will have the "other" permissions on */bin/*.
5. `touch /bin/testing `
- > User student does not have the **write** permission in */bin/*.  Only the owner of */bin/* - the admin **root** account - could write to */bin/* but all users have **read** and **execute** permissions.
6. `cd ; pwd `
- > Confirm you are working in */home/student/* again.
7. `stat Desktop `
- > Notice that `stat` shows owner, group, and permissions similar to `ls -l` and more.

![image](https://user-images.githubusercontent.com/36435980/145905897-b177d584-9eed-4e6b-8490-88457bebacf8.png)

8. `stat --help | less `  
- > Note that the `--format=FORMAT` or `-c FORMAT` options  will display only the sequences specified.

![image](https://user-images.githubusercontent.com/36435980/145906254-c5fcdc35-65d3-4a47-8a9d-9fe5767a368c.png)

9. `echo "The octal permissions for ~/Desktop are $(stat -c %a  ~/Desktop/)." 
10. `echo "The symbolic permissions for ~/Desktop are $(stat -c %A  ~/Desktop/)." 

![image](https://user-images.githubusercontent.com/36435980/145906612-919bbcff-2a0a-4dbe-b66f-f265a1635193.png)

*****

*****

*****
