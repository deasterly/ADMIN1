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
