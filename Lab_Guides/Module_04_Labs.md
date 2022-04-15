# WORKING WITH FILES
## GNU Coreutils

### TRY IT - Using Essential File and Directory Commands

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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
# WORKING WITH FILES
## GNU Coreutils

## TRY IT - Using Symbolic Links

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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
# WORKING WITH FILES
## GNU Coreutils

### TRY IT - Using Hard Links 

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `cd  /usr/share/zoneinfo/ `
3. `file  UTC `
4. `ls  -l /usr/share/zoneinfo/UTC `
5. `stat  UTC `
- > Notice the "link count" column from the output of `ls -l` and the "Links:" field from `stat` show the same value.
6. `find  -samefile  UTC `
7. `find  -samefile  UTC   | wc  -l `
- > Notice there are 8 hard links to the file */usr/share/zoneinfo/UTC*.
8. `ls   -li   $(  find  -samefile  UTC  ) `
- > Notice all 8 hard links point to the same **"inode"** on the filesystem.

![image](https://user-images.githubusercontent.com/36435980/145094499-d74767a0-cce3-4065-acb2-9905f8000189.png)

9. `cd ; pwd `
- > Make sure you are working in */home/student/*  again.  
10. `cp   -v   /usr/share/dict/words   ~/ `  
11. `ls   -lih ~/words `
- > Notice the inode number of *./words*.
12. `cp  -v  words   words1 ;   ls  -lih  words* ` 
- > Notice the copy has a different inode and both files have a link count of one.
13. `ln   words1   words2  ;   ls   -lih  words* `
- > Notice the link count incremented to 2 and the hard links share the same inode.
14. `ln  words1   words3  ;  ls -lih  words*  `
- > Notice the link count incremented again and the inode remains the same.
15. `rm   -v   words1    ;   ls  -lih  words* `
- > Notice the only change was the link count decreased by 1.
16. `rm   -v   words2   ;   ls   -lih   words* `
- > Notice that *words3* has a link count of 1 like a regular file.
17. `rm   -v  words* `

![image](https://user-images.githubusercontent.com/36435980/145095117-ae9cdfc4-09f9-43e9-ba05-01470b8607ce.png)

******
# GNU COREUTILS
## Lesson Summary

### HANDS ON EXERCISE - Managing Files, Directories, and Links

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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
# ARCHIVING
## Using the `tar` Tape Archiver

### TRY IT - Tar Archiving

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `tar --help | less `
- > Review the *EXAMPLES* and *Compression Options* in the help then exit `less` when done.
3. `mkdir -v /tmp/backup  /tmp/restore `
4. `sudo tar  -cf  /tmp/backup/backup.tar   /etc    /var/log    /root `
- > Note that `tar` removes leading forward slashes from file paths to make the archive contents a *relative path* rather than the *absolute path* that was used in the command.
5. `sudo  tar  -caf  /tmp/backup/backup.tar.xz    /etc   /var/log    /root `
6. `ls  -ahl  /tmp/backup/ `
- Compare the sizes of the compressed and uncompressed archives.

![image](https://user-images.githubusercontent.com/36435980/145628348-379ecb04-47b3-4ef5-935c-b6bb8ff13b69.png)

7. `cd  /tmp/restore `
8. `file  /tmp/backup/* `
9. `sudo  tar  -tvf  /tmp/backup/backup.tar.xz | less `
- > Note that the `tar` archive preserves important information like ownership, permissions, and timestamps.
10. `sudo  tar  -xf  /tmp/backup/backup.tar.xz  `
11. `ls  -lh `

![image](https://user-images.githubusercontent.com/36435980/145628567-a8ba1086-c27e-41cf-962d-6078d6479392.png)

*****
# ARCHIVING (Pages 71-75)
## Lesson Review

### HANDS ON EXERCISE - Managing and Archiving Files

> Perform the following tasks on the **Workstation VM** as user **student**.
******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh root@192.168.4.3 `
- > Enter **Passw0rd!** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `hostname ; whoami ; pwd`
- > Confirm you are logged in to **SERVER1** and are starting from the **~root** home directory.
5. Open a second terminal on the **Workstation VM** as user **student** and type this command:
6. `tar --help | less `
- > Refer to this terminal for help as needed and exit `less` when done.
*****
### STEP 3: Complete the following steps on SERVER1
1. Open the ***Pearson RHCSA 8 Cert Guide*** to page 75 
2. Complete **Exercise 3-5** from the book

******
# WORKING WITH FILES (pages 62-63, 67-68)
## Module Review

### END OF MODULE LAB - Working with Files

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### STEP 3:  Perform the following operations on SERVER2
1. Open the ***Pearson RHCSA 8 Cert Guide*** to pages 62-63 
2. Complete **Exercise 3-2** from the book
3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 67-68
4. Complete **Exercise 3-3** from the book

******
