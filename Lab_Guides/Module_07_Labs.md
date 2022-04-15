# PERMISSION BASICS
## The User/Group/Other and Read/Write/Execute Permissions Model

## TRY IT - Viewing and Interpreting Permissions

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

9. `echo "The octal permissions for ~/Desktop are $(stat -c %a  ~/Desktop/)."  `
10. `echo "The symbolic permissions for ~/Desktop are $(stat -c %A  ~/Desktop/)."  ` 

![image](https://user-images.githubusercontent.com/36435980/145906612-919bbcff-2a0a-4dbe-b66f-f265a1635193.png)

*****
# PERMISSIONS BASICS
## Setting Ownership and Permissions

### TRY IT - Setting File Ownership and Permissions

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `pinfo chown  `
- > Read down to the paragraph ending with `*Note Disambiguating names and IDs::`
3. `pinfo coreutils --node="File permissions" `
- > Refer to this documentation for more information about *Symbolic Modes* and *Numeric Modes* as needed.
4. `chmod --help `
- > Note that multiple *Symbolic Modes* can be separated by commas.
- > The **OCTAL-MODE** is explained in the *coreutils.info* under *Numeric Modes*. 
5. `cp /usr/share/dict/words ~/ `
6. `ls -l words `
7. `id `
- > Confirm you are a member of the group **wheel**.
8. `chown -v  :wheel words `
- > Note that the owner of a file or directory can only change the group ownership if they are members of that group.
9. `chown -v  root:root words `
- > Note the error message.  Administrative privileges are required to change the owner to any other user or the group owner to any group of which you are not a member.
10. `chmod -v a=rw words `
- This give everyone **read** and **write** on the file.  Note the OCTAL permission numbers.
11. `chmod -v o-rw words `
- > This removes **read** and **write** from **other**.  Note the OCTAL permission numbers.
12. `chmod -v g=r  words `
- > This gives the owning group **read** only.  Note the OCTAL permission numbers. 

![image](https://user-images.githubusercontent.com/36435980/146073942-8e85def7-c00a-4c5c-a84b-65d3a5f74701.png)

*****

# PERMISSIONS BASICS
## Lesson Review

### HANDS ON EXERCISE - Basic Permissions Practice

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `sudo -i `
5. `ls -lh /home `
- > Confirm the users **bob** and **joe** created in an earlier lab exist.  Recreate the accounts if needed.
6. `id bob ; id joe `
- > Confirm **bob** is a member of the group **managers** and **joe** is a member of the group **wheel**.
- > Recreate groups and modify users as needed.
7. `su -l  joe `

![image](https://user-images.githubusercontent.com/36435980/146076307-ef755058-cb47-48cb-8693-c470a8419289.png)

8. `sudo mkdir -v /home/reports `
9. `ls -ld /home/reports `
10. `sudo chown -v joe:managers /home/reports ` 
11. `sudo chmod -v  u=rwx,g=rx,o-rwx  /home/reports  `
- > This combination of ownership and permissions allows **joe** full control over */home/reports/* while allowing **bob** or any other member of **managers** read-only access to the contents.

![image](https://user-images.githubusercontent.com/36435980/146077332-1bcc61e8-d8d6-46d6-b4cf-38c36ca562e7.png)

12. `cd /home/reports `
13. `df -h > filesystems_report.txt `
14. `lsblk > disk_report.txt `
15. `ls -lh `
16. `exit `
17. `su -l bob `
18. `cd /home/reports `
19. `mkdir -v managers `
- > Notice the error message.  The group **managers** does not have the **write** permission.
20. `cat filesystem_report.txt `
21. `rm --force  disk_report.txt `
- > The **write** permission on the parent directory is required to delete a file.
22. `exit `
23. `exit `
24. `exit `
- > Log out of **SERVER1** completely.

![image](https://user-images.githubusercontent.com/36435980/146079499-4a051b5a-cf38-4336-807c-ec5e1f009dc9.png)

******
# SPECIAL PERMISSIONS
## Adding and Removing Special Permissions

### TRY IT - Setting Special Permissions

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ls -ld  /tmp   /run/log/journal   /bin/passwd  `
- > Note the **other** permissons on */tmp/*.
- > Note the **group** permissons on */run/log/journal/*.
- > Note the **owner** permissions on */bin/passwd*.
3. `file /tmp   /run/log/journal   /bin/passwd  `

![image](https://user-images.githubusercontent.com/36435980/146269203-c29f2912-0d96-44cc-9f5b-d9e27cf2ae3c.png)

4. `mkdir /tmp/testdir `
5. `stat /tmp/testdir `

![image](https://user-images.githubusercontent.com/36435980/146269387-19c1e307-977a-4240-96ac-4b3b483deeef.png)

6. `chmod -v o+t  /tmp/testdir  `
7. `file /tmp/testdir  `
8. `ls -ld /tmp/testdir `
9. `chmod -v o-t /tmp/testdir `
10. `file /tmp/testdir  `

![image](https://user-images.githubusercontent.com/36435980/146269777-3ee71be1-2feb-44a1-9c98-cf0a93ce8ca3.png)

11. `chmod -v g+s /tmp/testdir ;  file  /tmp/testdir `
12. `chmod -v 3770  /tmp/testdir  ; file /tmp/testdir  `  
13. `stat /tmp/testdir  `
14. `rm -vrf /tmp/testdir  `

![image](https://user-images.githubusercontent.com/36435980/146270382-723a2634-68ce-4706-a038-a49c1c0d0094.png)

******

# SPECIAL PERMISSIONS
## Lesson Review

### HANDS ON EXERCISE - Creating a directory for Group Collaboration

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `sudo -i `
5. `ls -lh /home `
- > Confirm the users **bob** and **joe** created in an earlier lab exist.  Recreate the accounts if needed.
6. `groupadd --gid 5555  devops  `
7. `usermod -aG devops bob ;  usermod -aG devops joe `
8. `id bob ; id joe `
- > Confirm **bob** and **joe** are now members of **devops**.
- > Recreate groups and modify users as needed.

![image](https://user-images.githubusercontent.com/36435980/146272261-75695004-7c2e-4d87-8ed3-30eb0386ab86.png)

9. `mkdir -pv  /home/devops/{public,private} `
10. `ls -alR /home/devops `

![image](https://user-images.githubusercontent.com/36435980/146272853-69d57157-51cd-42d5-8652-26dc800174ae.png)

11. `chown -Rv  :devops  /home/devops  `
12. `chmod -v u=rwx,g=rwxs,o=rxt  /home/devops/public `
13. `chmod -v 3770  /home/devops/private `
14. `ls -lR  /home/devops  `
- > As members of **devops** both **bob** and **joe** should have full access to both *collaboration directories*.
- > Because **student** in neither the owner nor a member of **devops** the **other** permissions will apply, allowing read-only access to */home/devops/public/* and no access to */home/devops/private/*.

![image](https://user-images.githubusercontent.com/36435980/146273645-ded7afc6-dc30-4568-b5ee-d2201d2a05ec.png)

15. `exit `
16. `exit `
- > Log out of **SERVER1** completely.

*****

# FILE PERMISSIONS (pages 152-156)
## Module Review

### END OF MODULE LAB - File Permissions

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### STEP 3:  Perform the following operations on SERVER2
1. `sudo -i `
2. Confirm the following users and groups are configured.  Create and modify as needed.

| USERS   | GROUPS              |
| :------ | :------------------ |
| linda   | linda, sales        |
| laura   | laura, sales        |

3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 152 
4. Complete **Exercise 7-1** from the book
- > Note that `passwd ` also has options to manage password aging policy similar to `chage `.
5. Open the ***Pearson RHCSA 8 Cert Guide*** to page 156 
6. Complete **Exercise 7-2** from the book

### SOLUTION


*****



*****

