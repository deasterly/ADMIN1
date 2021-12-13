# PASSWORD AGING POLICIES
## Policy Settings and Configuration Files

### TRY IT - Viewing Password Policy Settings

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
2. `man chage  `
3. Read the manual and find answers to the following questions:
    1. What 6 parameters can be set with the **OPTIONS** for `chage`?
    2. When using the `-E` or `--expiredate` option, what argument will remove an account expiration date?
    3. According the the **OPTIONS** section of the manual, what happens when `chage LOGIN ` is run with no options selected?
    4. According to the **NOTE** section, which option for `chage` is **not restricted to root** for unprivileged users to determine their password or account expiration dates?
    5. Which 3 configuration files are mentioned under the **CONFIGURATION** and **FILES** sections of the manual?

4. `man 5 shadow `
5. Read the manual and find answers to the following question:
    1.  Which character in the second field indicates a locked password?
    2.  What does a `0` in the third field mean?
    3.  What does it mean if the seventh field is empty?
  
6. `chage -l student `
7. `chage -l user2 `
- > Note that admin privileges are required to see information about users other than yourself.
8. `sudo !chage `

![image](https://user-images.githubusercontent.com/36435980/145695570-5bc7c487-17c1-4a9c-bce9-fd7d8112897e.png)

9. `sudo grep 'user2' /etc/shadow `
10. `sudo chage user2   `
- Change only the following values:
    1. Maximum Password Age: 90
    2. Password Expiration Warning: 10
    3. Password Inactive: 14
11. `sudo grep 'user2' /etc/shadow `
- > Which fields changed?

![image](https://user-images.githubusercontent.com/36435980/145695697-3ffea619-47e9-459c-993e-9953e2f591e4.png)

12. `sudo chage -l user2 `
13. `sudo chage --lastday 0  user2 `
14. `sudo chage -l  user2 `

![image](https://user-images.githubusercontent.com/36435980/145695746-a49bcf99-b8e2-45b4-b5fa-7d022e371280.png)

15. `ssh user2@localhost `
- > Note that **user2** must enter the current password before entering the new password!
- > Set the password to a more secure password of your choice (**PassTheEX200!!** for example).
- > The user will be logged out and must reconnect after changing their password.
16. `ssh user2@localhost `
- > Enter the NEW password when prompted.

![image](https://user-images.githubusercontent.com/36435980/145695902-20e68c70-0fa4-4328-a52a-684f6f5d2fbf.png)

*****

*****

*****

