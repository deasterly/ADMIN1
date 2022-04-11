# LOCAL USERS AND GROUPS
## User Management

### TRY IT - Managing Local Users

> ### Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `grep 'student'  /etc/passwd  /etc/group  `
3. `id student `
4. `useradd --help | less `
- > Notice the options for setting the UID number, GECOS comment, home directory, shell, and group memberships with `useradd`.
5. `sudo useradd user1`
6. `sudo useradd -u 3002 -c "Test User 2" user2  `
7. `sudo useradd -G cdrom,wheel,group0  -c "Test User 3"  user3 ` 
8. `grep  'user[0-9]'  /etc/passwd   /etc/group ` 

![image](https://user-images.githubusercontent.com/36435980/145649290-6556e76a-5ad5-41ca-b39c-8f56314a3867.png)

9. `usermod --help | less `
- > Notice that most options for `useradd` and `usermod` are similar.  
10. `sudo usermod --comment "Test User 1" --groups group0  user1 `
11. `getent passwd user1 `
12. `sudo usermod --uid 3001  user1  `
13. `grep 'user1'  /etc/passwd   /etc/group  `

![image](https://user-images.githubusercontent.com/36435980/145650351-5a8cbcd8-03e7-4aad-8df8-98e3fb3eccdd.png)

14. `ls /home `
- Notice the home directories for the 3 test users.
15. `sudo find  /   -user  user3  2>  /dev/null `
- > This finds all files belonging to **user3**  while ` 2>  /dev/null ` discards errors such as "Permission denied."
16. `sudo userdel  -r  user3 `
17. `sudo find  /  -user  user3 `
18. `ls /home `
- > Notice that the account for **user3** no longer exists. 

![image](https://user-images.githubusercontent.com/36435980/145651650-f6f13cd5-8b0f-43d9-be98-8d3f8f74209e.png)

19. `sudo passwd user1 `
- > Set the password to **Passw0rd** when prompted.
20. `sudo -i `
- > Only an administrator can set another user's password.
21. `echo  Passw0rd | passwd --stdin  user2 ` 
- > Notice this method allows passwords to be set without typing them twice.
22. `exit `

![image](https://user-images.githubusercontent.com/36435980/145652699-72950846-ad72-4a71-9c4c-d0a63ce3225e.png)

23. `ssh user1@localhost`
- > Enter the password set in a previous step.
24. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the **Workstation VM** and are working the the ***~user1*** home directory.
25. `passwd `
- > Change the password for **user1** to a more secure password of your choice (**PassTheEX200!!** for example).
- > Pay attention to the prompts!  Users must enter their CURRENT password before entering the new password with `passwd`.
26. `exit `
27. `ssh user1@localhost `
- > Confirm the new password for **user1** works correctly.

![image](https://user-images.githubusercontent.com/36435980/145652872-e3adf68c-c6f1-4668-b2d4-2b955b6cf153.png)

*****

*****

*****
