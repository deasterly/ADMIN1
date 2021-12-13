# INPUT/OUTPUT REDIRECTION
## Lesson Review

### HANDS ON EXERCISE - Using I/O Redirection and Pipelines

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~USER** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `find / -name messages | less `

![image](https://user-images.githubusercontent.com/36435980/144673204-249c26bd-0000-4c50-8bc1-5ae725f810de.png)
![image](https://user-images.githubusercontent.com/36435980/144673290-166b00c0-4788-4546-9568-fbbba2dfaeb9.png)

5. `find / -name messages  2>/dev/null `
6. `find / -iname messages 2>/dev/null `
7. `find /usr -name words 2>/dev/null `
8. `find / -name *.pdf 2>/dev/null `
9. `find / -iname *.jpg 2> /dev/null `
10. `find / -size +10M 2>/dev/null `

![image](https://user-images.githubusercontent.com/36435980/144673520-b013d4dd-8b54-42f2-a36d-4eb204f28b93.png)

11. `find / -iname *.pdf -exec cp  -v  {} ~ \;   2> /dev/null `
12. `cd  ;  pwd `
13. `ls -lah | tee ~/my_dir_list.txt `
14. `head -n5 my_dir_list.txt > top5.txt `
15. `tail -n3 my_dir_list.txt > last3.txt `
16. `head -n 15 /usr/share/dict/words | tee  ~/words.txt `
17. `wc -l ~/words.txt `

![image](https://user-images.githubusercontent.com/36435980/144673799-a4dea511-3a79-41d0-914d-f5006ca35db4.png)

******
