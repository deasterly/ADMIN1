# Documentation
## Lesson Review

### HANDS ON EXERCISE - Searching and Using Documentation

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
2. `ssh student@192.168.4.3 `
- > Enter ***Passw0rd*** for the password when prompted.  
3. Type the following in the SSH terminal on server1
4. `man apropos ` 
- > Read the **DESCRIPTION** and **SEE ALSO** sections of the manual.
5. `man -k mandb `
6. `man mandb `
7. `mandb `
- > Note that user **student** does not have permission to update the manual search index.

![image](https://user-images.githubusercontent.com/36435980/144495199-d663bb92-97f0-40aa-b652-4388bdf5292d.png)

8. `sudo mandb `

![image](https://user-images.githubusercontent.com/36435980/144495290-7ffd921c-3174-44b1-8b8e-202385916c26.png)

9. `man -k mandb manuals documentation `

![image](https://user-images.githubusercontent.com/36435980/144495381-8a408d06-b6a8-43e9-8206-3c573c1f2f1f.png)

10. `man -f passwd `
11. `whatis passwd `
12. `man 5 passwd `
- > Notice section 5 covers configuration files.
13. `man 1 passwd `
- > Notice section 1 covers commands.
14. `man -K passwd `

![image](https://user-images.githubusercontent.com/36435980/144495791-c4b2acf3-425a-487e-9b53-c7f1f49ae281.png)

15. `pinfo pinfo `
- > If you want to fully understand all the keybindings in `pinfo` take a look at the "Configuration file," "Example config file" and "Keybindings" nodes.

![image](https://user-images.githubusercontent.com/36435980/144496339-146c3c00-3534-4ed3-8b3b-7755f4f23eb4.png)

16. `pinfo bash `
- Navigate to the **" \* Introduction::"** node.
![image](https://user-images.githubusercontent.com/36435980/144496516-a5a1ca57-b0e9-470c-b041-dfeb028b9b10.png)

- Read the "What is Bash?" and "What is a shell?" nodes.)
![image](https://user-images.githubusercontent.com/36435980/144496571-9a559d63-e598-4352-aaf0-d0645bed1194.png)

******
