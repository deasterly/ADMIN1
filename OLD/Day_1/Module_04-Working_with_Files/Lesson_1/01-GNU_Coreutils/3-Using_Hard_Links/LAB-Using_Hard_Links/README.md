# WORKING WITH FILES
## GNU Coreutils

### TRY IT - Using Hard Links 

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
