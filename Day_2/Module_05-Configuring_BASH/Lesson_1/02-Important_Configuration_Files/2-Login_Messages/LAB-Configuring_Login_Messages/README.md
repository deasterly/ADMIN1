# CONFIGURING BASH
## Important Configuration Files

### TRY IT - Configuring Login Messages

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
2. `man 5 issue  motd  `
- > Read both manuals completely.
3. `cp -v /etc/motd  /tmp/motd.bak `
4. `vim /etc/motd `
- Add the following line:
```
Welcome to Workstaton
```
5. `ssh localhost`
- > After authenticating as user **student** look for the new MOTD.
6. `exit`

![image](https://user-images.githubusercontent.com/36435980/145639864-f2e9da26-ac7b-40b0-9429-a4b47419ce52.png)

*****
