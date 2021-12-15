# SPECIAL PERMISSIONS
## Lesson Review

### HANDS ON EXERCISE - Creating a directory for Group Collaboration

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

*****

*****
