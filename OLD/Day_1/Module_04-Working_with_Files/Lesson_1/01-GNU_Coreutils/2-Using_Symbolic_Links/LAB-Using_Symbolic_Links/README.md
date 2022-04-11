# WORKING WITH FILES
## GNU Coreutils

## TRY IT - Using Symbolic Links

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
2. `ln --help | less `
- > Notice the usage example, default behavior, and options.

![image](https://user-images.githubusercontent.com/36435980/145092295-e390d021-46fe-4f02-af72-252264e261a6.png)

3. `file  /usr/tmp `
4. `ls -l /usr/tmp `
- > Notice there is NO TRAILING SLASH in the */usr/tmp*  path.
5. `ls -l /usr/tmp/ `
- > Notice the contents of the TARGET directory are shown with the trailing slash.
6. `cd ; pwd `
- > Make sure you are working in */home/student* first.
7. `ln  ~/Pictures   ~/Photos `
- > Notice the error message.  **Links to a directory must be symbolic.**
8. `ln  -s   ~/Pictures  ~/Photos `
9. `file Photos `
10. `stat Photos `

![image](https://user-images.githubusercontent.com/36435980/145092404-7ccf4b11-0b9b-4fad-8864-3817c9a3441f.png)

11. `sudo -i `
- > Enter ***Passw0rd*** when prompted for the password.
12. `pwd `
- > Make sure you are working in */root/* first.
13. `ln  /etc/hostname   /boot/ `   
- > Read the error message.  `"Invalid cross-device link"` means the TARGET and LINK are on different filesystems.
14. `ln -s  /etc/hostname   /boot/ ` 
15. `file   /boot/hostname  `
16. `ls -l  /boot/hostname `
17. `cat   /boot/hostname `
18. `rm   /boot/hostname `  
- > Type **`<y><ENTER>`** when prompted.   
19. `exit `
- > Return to the **student** user account.
20. `rm -v   ~/Photos `
21. `ls   ~ `

![image](https://user-images.githubusercontent.com/36435980/145093073-34e55575-0994-4dca-84d1-2b6b7501f8ec.png)

******
