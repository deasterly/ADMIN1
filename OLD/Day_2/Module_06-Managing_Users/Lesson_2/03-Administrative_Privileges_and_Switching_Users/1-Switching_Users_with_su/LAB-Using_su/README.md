# MANAGING USERS
## Administrative Privileges and Switching Users

### TRY IT - Using `su`

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
2. `su --help | head -n 15  `
- > Review the syntax and options for the `su` command.

![image](https://user-images.githubusercontent.com/36435980/145692673-e2897a5c-e1e0-4dcd-8f36-898a12dad771.png)

3. `whoami `
4. `su --login `
- > Or use the equivalent `su -l` or `su - `. There are always many ways to get the desired results in the CLI shell.
- > Enter **Passw0rd!** when prompted.
5. `whoami ; pwd `
6.  `su -c "whoami ; pwd" user1  `
- > If the **user1** account was not created in the previous lab OR the Workstation VM was reset to an earlier snapshot where **user1** does not exist, recreate the account.
- > Note that the `su` command does not prompt the **root** user for passwords! 
7. `su -lc "whoami ; pwd"  user1 `
- > Note the difference between the PWD when using a non-login shell ( */root/* ) and a login shell ( */home/user1/* ).  
8. `exit `

![image](https://user-images.githubusercontent.com/36435980/145692898-fb0ac31e-b019-49a0-a0a0-e12664f64d53.png)

9. `id user2 `
- > Confirm **user2** exists.  Create the account and set or change the password to **Passw0rd** as needed.
10. `su -  user2 `
11. `id ; pwd ; echo $PATH `
- > Note the environment with a *login shell*.
12. ` exit `
13. `su user2 `
14. `id ; pwd ; echo $PATH `
- > Note the difference in the environment with a *non-login shell*.
15. `exit `

![image](https://user-images.githubusercontent.com/36435980/145693534-e6a3337b-650d-430b-8ece-c4034e915e88.png)


******

******

******

