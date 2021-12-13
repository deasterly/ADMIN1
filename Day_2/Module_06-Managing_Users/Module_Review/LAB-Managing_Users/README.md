# MANAGING USERS (pages 135-138)
## Module Review

### END OF MODULE LAB - Managing Users

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
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
1. `sudo -i `
2. `cp -v /etc/login.defs ~/ `

3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 135 
4. Complete **Exercise 6-2** from the book
- > Note that `passwd ` also has options to manage password aging policy similar to `chage `.
5. Open the ***Pearson RHCSA 8 Cert Guide*** to page 138 
6. Complete **Exercise 6-3** from the book

******

******

******
