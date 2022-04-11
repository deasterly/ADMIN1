# TYPES OF COMMANDS
## Lesson Review

### HANDS ON EXERCISE - Using Commands and Aliases

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
4. `ps<TAB>`
- > Notice nothing happens with a single **`<TAB>`**.
5. `ps<TAB x2> `
- > Notice the options available to us that start with the letters `ps`
6. `pst<TAB> `
- > BASH now has enough characters to autocomplete the command unambiguously.
7. `pstree ` 
8. `cd /etc`
9. `cat gro<TAB  x2> `
- > Note that the possible matches are still ambiguous.
10. `cat grou<TAB> `
- > A single **`<TAB>`** autocompletes when there are no other possible matches.
11. `cat group | wc -w `
- > Count the number of "words" (as understood by  `wc`)
	
### TASK 3: Use expansion with commands and aliases
1. Type the following in the SSH terminal on **server1**
2. `cd ~ ` 
3. `date --help | less `
- > Note the FORMAT string options for MM/DD/YY dates, HH:MM:SS times, weekday names, and others that may be useful.
4. `echo "Today is $(date +%A) $(date +%D) and the current time is $(date +%r)." `
5. `file $(which uptime) `
6. `file /usr/share/dict/linux.words `
7. `wc -l /usr/share/dict/linux.words `

![image](https://user-images.githubusercontent.com/36435980/144326265-d04352e0-9e2f-4210-99c3-18e85c837798.png)

8. `alias today='echo "Today is $(date +%A), $(date +%D) and the current time is $(date +%r)."  ' `
9. `which today `
10. `today `
11. `logout `

![image](https://user-images.githubusercontent.com/36435980/144326525-4b343fb5-99f4-4fd4-b5b5-ca608fa145da.png)
	
### TASK 4: Complete the following operations	
1. Return to the terminal on Workstation and type the following:
2. `alias -p `
3. `which labtest `
- > Note that this will only work as shown if the SSH connection to **server1** was made from the same shell where this alias was created.
4. `unalias labtest `
5. `which labtest `

![image](https://user-images.githubusercontent.com/36435980/144327077-b75e8b06-f312-4e84-bb2e-c23a557831d6.png)

6. `echo $SHELL `
7. `cat /etc/shells `
8. `sudo yum -y install zsh `

![image](https://user-images.githubusercontent.com/36435980/144327326-01591696-e2f1-46b4-ada0-75925490d90a.png)

10. `cat /etc/shells `
11. `exit `
	
![image](https://user-images.githubusercontent.com/36435980/144327378-9c98e3c4-7f0b-490a-9b2f-4c3d47ce1ac3.png)
	
******
