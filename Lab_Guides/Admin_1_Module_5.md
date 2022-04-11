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
# CONFIGURING BASH
## Shell Environment Configuration

### TRY IT - Personalizing the Shell Environment

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
2. `ls /etc/bash* /etc/profile* ~/.bash*  `
3. `pinfo bash --node="Bash Startup Files"  `
- > Note the order in which startup files are processed for an *interactive login shell*.
    1. First process */etc/profile* and */etc/profile.d/*.sh* "include* files.
    2. Then process *~/.bash_profile* (or */.bash_login* or *~/.profile*  if the previous file does not exist).
    3. The *~/.bash_profile* checks for and processes *~/.bashrc* if the file exists.
    4. The *~/.bashrc* checks for and processes */etc/bashrc* if the file exists.
    5. The *~/.bashrc* then processes any commands that appear **after** the */etc/bashrc* has been processed. 

![image](https://user-images.githubusercontent.com/36435980/145634542-62a6caf2-4478-4273-a99e-52276a64f29e.png)

![image](https://user-images.githubusercontent.com/36435980/145634352-e058a1cb-1953-405c-8175-b379ef7a7aaa.png)

4. `cat ~/.bash_profile `
5. `head ~/.bashrc `
- > Note that without the command  `.  ~/.bashrc` in *~/.bash_profile* then *~/.bashrc* will not be called to run `.  /etc/bashrc`.

![image](https://user-images.githubusercontent.com/36435980/145635240-5440b80f-0bff-490a-be24-9eff66ba7414.png)

6. `tail /etc/profile `
- > Note the comments. If the variable `BASH_VERSION` is a non-empty string AND */etc/bashrc* is a file then */etc/bashrc* is called by running `.  /etc/bashrc `.  
7. Change the **student** user's `PS1` variable in the file *~/.bashrc* to `'[\u@\h \t \w]\$ '` to add the time to the prompt.
    1. `echo $PS1 `
    2. `vim  ~/.bashrc `
    3. Add the following line at the bottom of the file:
  ```
  export PS1='[\u@\h \t \w]\$ '
  ```
  - > Note the SPACE after the \$ and before the closing single quote.
    4. `.   ~/.bashrc`
  - > Note the PROMPT updated to include the time.
 
 ![image](https://user-images.githubusercontent.com/36435980/145637599-1e1a273f-3a1c-4933-b479-610168bb3e84.png)

 8. Undo the previous change by deleting the new line from */.bashrc*
 9. Logout of the terminal and open a new terminal to confirm the time no longer appears in the prompt.
 
![image](https://user-images.githubusercontent.com/36435980/145637679-e7645fd7-71f5-4aeb-9be0-824e81ba5859.png)

*****
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
# CONFIGURING BASH (pages 42-44)
## Module Review

### END OF MODULE LAB - Configuring BASH

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### TASK 3:  Perform the following operations on SERVER2
1. Create a user named **user** with a password of **Passw0rd** on SERVER2
2. `sudo useradd user `
3. `echo Passw0rd | sudo passwd --stdin  user `
4. `ssh  user@localhost `
- > Enter **Passw0rd** when prompted.

![image](https://user-images.githubusercontent.com/36435980/145645524-edc442a4-3fd9-4fa2-b77e-68107060e324.png)

5. Open the ***Pearson RHCSA 8 Cert Guide*** to page 44 
6. Complete **Exercise 2-6** from the book
- > Run  `ssh  user@localhost ` when asked to open another shell as **user**.

******
