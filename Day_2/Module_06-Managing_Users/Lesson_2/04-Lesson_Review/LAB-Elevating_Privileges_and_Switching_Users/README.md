# ADMINISTRIATIVE PRIVILEGES AND SWITCHING USERS
## Lesson Review

### HANDS ON EXERCISE - Elevating Privileges and Switching Users

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
4. `id bob`
- > Confirm the user **bob** from an earlier lab exists. Create the account and set the password to **Passw0rd** as needed.
5. `sudo -i `
6. `man visudo `
- > Read to the end of the second paragraph of the **DESCRIPTION** section of the manual.

![image](https://user-images.githubusercontent.com/36435980/145694622-8bb430be-c82f-4cd0-a0ed-5776db9fa816.png)

7. `man sudoers `
- Press **`</>`** slash to open a SEARCH prompt.
- Type `sudoers.d**<ENTER>**` and read the manual down to the paragraph explaining which characters in a file name under */etc/sudoers.d/* would exclude the file from being processed by the **#includedir** directive.

![image](https://user-images.githubusercontent.com/36435980/145694583-1488d006-e3e8-43ec-bccb-1b1357487e6e.png)

*****
### TASK 3: Configure `sudo` 
1. Configure `sudo` to allow user **bob** full admin privileges without a password. Type these commands in the terminal: 
2. `grep 'NOPASSWD' /etc/sudoers  `
- > Use this example to begin.
3. `grep 'NOPASSWD' /etc/sudoers  > /etc/sudoers.d/bob `
4. Make the file */etc/sudoers.d/bob* contain the following text:

```
bob  ALL=(ALL)    NOPASSWD:  ALL
```
- > Use I/O redirection or `vim /etc/sudoers.d/bob` as preferred
- > Adding this line at the bottom of the file */etc/sudoers* with the command `visudo` would have the same effect.
5. Log in to the **bob** account and confirm the `sudo` command works without a password.
    1. `su - bob `
    2. `whoami `
    3. `sudo whoami `
    4. `exit `
  
![image](https://user-images.githubusercontent.com/36435980/145694901-d9d4c0a3-4779-4a28-a116-0cdf52adafee.png)


*****

*****

*****
