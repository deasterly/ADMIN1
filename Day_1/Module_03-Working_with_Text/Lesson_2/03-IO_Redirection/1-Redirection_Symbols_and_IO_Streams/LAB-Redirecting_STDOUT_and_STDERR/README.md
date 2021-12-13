# INPUT/OUTPUT REDIRECTION
## Redirection Symbols and I/O Streams

### TRY IT - Redirecting STDOUT and STDERR

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
2. `ll -R /tmp `
- > Notice some lines show files or directories - ***STDOUT*** -  while other lines - ***STDERR*** - are errors.

![image](https://user-images.githubusercontent.com/36435980/144664087-d17fa012-793b-4b5d-8faf-f7c6ac4e00c2.png)

3. `ll -R /tmp 2> /dev/null `
- > Notice the errors are discarded.
4. `ll -R /tmp &>  ~/tmpfiles1.txt `
5. `wc -l ~/tmpfiles1.txt `
- > Notice the total number of lines includes both STDOUT and STDERR.
6. `ll -R /tmp >  ~/tmpfiles1.txt `
- > Notice that STDERR goes to the terminal and STDOUT goes to the file.

![image](https://user-images.githubusercontent.com/36435980/144664146-b7ef0747-905d-4ac4-8236-d012256f4ee5.png)
		
7. `wc -l ~/tmpfiles1.txt `
- > Notice there are fewer lines.
8. `ll -R /tmp 2>  ~/tmpfiles1.txt 
- > Notice that STDOUT goes to the terminal and STDERR goes to the file.
9. `wc -l ~/tmpfiles1.txt `
- > Notice there are fewer lines.

![image](https://user-images.githubusercontent.com/36435980/144664232-7fa5f69a-0c24-4771-b98b-77c6309fa651.png)
		
10. `ll -R /tmp >>  ~/tmpfiles1.txt 2> /dev/null `
- > Notice that STDOUT goes to the file and STDERR is discarded.
11. `wc -l ~/tmpfiles1.txt `
- > Notice the lines have been appended to the file.

![image](https://user-images.githubusercontent.com/36435980/144664286-bf18d40f-e3ee-4ca4-8711-3034a0c23c67.png)

******
