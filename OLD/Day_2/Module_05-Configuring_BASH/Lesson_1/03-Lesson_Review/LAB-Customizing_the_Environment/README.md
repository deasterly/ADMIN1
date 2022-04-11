# CONFIGURING BASH
## Lesson Review

### HANDS ON EXERCISE - Customizing the Environment

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
4. `printenv | less `
- > Review the environment variables and note which ones might be useful in commands.
5. `mkdir  -v  ~/scripts  `
6. `echo $PATH `
- > Note that */home/student/scripts/* is **NOT** part of the `PATH` variable.
7. `cp -v  ~/.bash_profile  /tmp/profile.bak `
8. `echo  "export PATH=${PATH}:/home/student/scripts" >> ~/.bash_profile `
- > Use I/O redirection or `vim` to add this line to *~/.bash_profile*
9. `tail -n 3  ~/.bash_profile `
- > Confirm that the `export PATH` line was appended to the END of the file and the remaining lines were NOT overwritten.
- > If the `export PATH` line is the **only** line, restore from the copy at */tmp/profile.bak* and try again.

![image](https://user-images.githubusercontent.com/36435980/145642598-49fd5d50-7dd0-42a7-870c-fcf2bf5d4cd4.png)

10. `vim ~/scripts/hello.sh `
- Add the following lines to the */home/student/scripts/hello.sh* file:
```
#!/bin/bash
echo "Hello $USER"
```
11. `chmod +x ~/scripts/hello.sh `
- > Permissions and the `chmod` command are covered in another module.
12. `which  hello.sh`
- > Read the error message.
13. `source  .bash_profile `
14. `echo $PATH `
15. `!which `
- > Note that `hello.sh` will run from the *~/scripts/* directory after updating the `PATH` 
16. `hello.sh `

*****
*****
*****
