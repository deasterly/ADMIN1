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

******

******
