# PASSWORD AGING POLICIES
## Lesson Review

### HANDS ON EXERCISE - Managing Users, Groups, Passwords, and Privileges

> Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `sudo -i `
5. `ls -lh /home `
- > Confirm the users **bob** and **joe** created in an earlier lab exist.  Recreate the accounts if needed.
6. `chage -l bob `

![image](https://user-images.githubusercontent.com/36435980/145896226-e1b38bed-283d-45a8-9c5d-08e4483e0c91.png)

7. Modify the policy settings for **bob** to the following:

| MIN PASS AGE | MAX PASS AGE | LAST PASS CHANGE | PASS EXPIRE WARNING | PASS INACTIVE | ACCOUNT EXPIRE DATE |
| :----------- | :----------- | :--------------- | :------------------ | :------------ | :------------------ |
| 3 DAYS       | 90 DAYS      | DO NOT CHANGE    | 10 DAYS             | 14 DAYS       | DO NOT CHANGE       |

8. `chage bob `
- > Follow the interactive prompts then confirm the correct settings were applied with `chage -l bob `

![image](https://user-images.githubusercontent.com/36435980/145897451-5170f874-54d1-4189-bde6-828394ef82e9.png)

9. `cp -v /etc/login.defs  ~/login.defs.bak `
- > Backup important config files before making changes!
- > Refer to `man login.defs` for more information as needed.
10. `vim  /etc/login.defs `

![image](https://user-images.githubusercontent.com/36435980/145897782-fd9f5b87-da50-4f59-8b7b-b83105f558ee.png)

11. Modify these lines in */etc/login.defs* as shown. 
```
PASS_MAX_DAYS        90
PASS_MIN_DAYS        3
PASS_MIN_LEN         5
PASS_WARN_AGE        10
```

![image](https://user-images.githubusercontent.com/36435980/145898458-a225b44b-7dbd-4352-a299-445798382a3d.png)

12. `chage -l joe `
- > Note that changing the defaults for new account creation in */etc/login.defs* will not change existing accounts!
13. `useradd -c "Bill Jones" bill `
14. `echo Passw0rd | passwd --stdin bill `
15. `chage -l bill `
- > Note that **bill** has the new password aging policy defaults from */etc/login.defs*.

![image](https://user-images.githubusercontent.com/36435980/145899240-6db748dd-649c-4924-a995-5c90e90f5367.png)

16. `exit `
17. `exit `
- > Log out of **SERVER1** completely.

******

******

******
