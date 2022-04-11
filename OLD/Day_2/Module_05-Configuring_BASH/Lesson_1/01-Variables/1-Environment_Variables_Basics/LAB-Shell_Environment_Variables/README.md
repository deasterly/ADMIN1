# CONFIGURING BASH
## Environment Variable Basics

### TRY IT - Shell Environment Variables

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
2. `printenv | grep -E 'USER|HOME|PATH|HOST|SHELL|PWD'  `
- > Note that these variables can be used in commands and will **expand** (following the rules for quoting and escaping) to their assigned values.
3. `echo $PS1 `
4. `OLDPROMPT=$PS1 `
5. `PS1='[TESTING]\$ '  `
6. `whoami ; pwd `
7. `PS1=$OLDPROMPT `
8. `echo "My home is at $HOME and my shell is $SHELL"  `

![image](https://user-images.githubusercontent.com/36435980/145631832-60cbab4f-8390-484f-b219-5cd5bdeb7342.png)

******
