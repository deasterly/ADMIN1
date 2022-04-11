# WORKING WITH FILES
## GNU Coreutils

### TRY IT - Using Essential File and Directory Commands

> ### Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `mkdir -v  ~/classfiles `
3. `cd ~/classfiles/ `
4. `mkdir -v test1 test2 test{3..5} `
5. `rmdir -v test* `
6. `touch test-{one,two,three} `
7. `ls -lh `
8. `rm -v test-t* `
9. `ls -lh `
10. `rm -v test* `

![image](https://user-images.githubusercontent.com/36435980/145090164-4cd4ea47-0ce9-4aa6-8e58-2b2874e7f5c3.png)

11. `mkdir -v dir1 dir2 `
12. `cp -v /usr/share/dict/words  dir1/ `
13. `rmdir dir1 `
- > Read the error message.
14. `cp -v dir1/words    dir2/words2 `
15. `mv -v dir1/words   dir1/words1 `
16. `mv -v dir2    dir1/subdir `
17. `ls -lhR `

![image](https://user-images.githubusercontent.com/36435980/145090503-fc672dce-f4ba-4d29-8d66-99dc0e6238b7.png)
	
18. `rm dir1 `
- > Read the error message.
19. `rm --help | grep 'directories' `
20. `rm --recursive --verbose dir1 `
21. `cd ; pwd `
- > Make sure you are working in */home/student/* again.
22. `rmdir -v  ~/classfiles ` 

![image](https://user-images.githubusercontent.com/36435980/145090977-6a9265f1-59a5-4307-9fd7-2ba8bd8c4112.png)

******
