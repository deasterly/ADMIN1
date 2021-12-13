# GNU COREUTILS
## Lesson Summary

### HANDS ON EXERCISE - Managing Files, Directories, and Links

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
3. Type the following in the SSH terminal on SERVER1
4. `ls -ahl `
5. `mkdir -v  ~/lab1  ~/lab2 `
6. `cp -v /usr/share/dict/linux.words ./ `
7. `cp -v linux.words words2 `
8. `cp -v words2 lab1/words3 `
9. `ls -l lab* `

![image](https://user-images.githubusercontent.com/36435980/145096271-d12d07f8-d1df-4a12-96f1-d1523633db17.png)

10. `ln /home/student/linux.words /tmp/linux.words-HL `
11. `find  /tmp  -samefile  ~/linux.words `
12. `ls -li  /tmp  /home/student `

![image](https://user-images.githubusercontent.com/36435980/145096420-c8be16ad-d8bc-4250-bffb-4f9735df8cde.png)
	
13. `mkdir -v /home/student/lab1/lab3 `
14. `ln -s  ~/lab1/lab3  ~/lab4 `
15. `file  ~/lab4 `
16. `	tree -l  lab* ` 
17. `ls  -lhR  lab* `
18. `mv  -v  ~/words2  ~/lab4 `
19. `tree  -l   lab* `

![image](https://user-images.githubusercontent.com/36435980/145099108-32c4f79a-ad6a-4441-82df-bf7529d3380c.png)
	
20. `rm -v ~/lab4 `
21. `rm -v ~/lab1 `
22. `rm -rv  ~/lab* linux.words *.txt `

![image](https://user-images.githubusercontent.com/36435980/145099247-5e1b435a-e1dd-4fcc-8539-25f1f1c1f7f6.png)

******
