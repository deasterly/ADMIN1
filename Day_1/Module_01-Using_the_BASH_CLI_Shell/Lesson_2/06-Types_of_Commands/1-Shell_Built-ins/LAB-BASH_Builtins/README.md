# TYPES OF COMMANDS
## Shell Builtins

## BASH Builtins

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `help | less ` 
- > Take a moment to read the top paragraph and list of built-in commands.

![image](https://user-images.githubusercontent.com/36435980/144315840-25f782be-217e-4d7c-bcf4-eaf4a5bafe67.png)

3. `rpm -ql bash | less `
- > Pay attention to all the files in */usr/bin/* that correspond to the BASH builtin commands

![image](https://user-images.githubusercontent.com/36435980/144316149-6a84def7-8da1-456e-a32a-8c80487ddf25.png)
	
4. `which cd `
5. `cat $(which cd) `
6. Review the `help` for the following builtin commands
- `help for `
- `help export `
- `help umask `

![image](https://user-images.githubusercontent.com/36435980/144316453-11000e03-6ed4-4e94-ac34-8c545c03aa5b.png)

*****
