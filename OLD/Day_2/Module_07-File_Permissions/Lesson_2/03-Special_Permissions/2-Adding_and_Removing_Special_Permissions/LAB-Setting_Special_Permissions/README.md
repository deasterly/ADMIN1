# SPECIAL PERMISSIONS
## Adding and Removing Special Permissions

### TRY IT - Setting Special Permissions

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
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

******

******
