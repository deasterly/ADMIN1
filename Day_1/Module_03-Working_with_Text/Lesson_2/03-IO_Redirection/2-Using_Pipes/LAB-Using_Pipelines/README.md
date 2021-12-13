# INPUT/OUTPUT REDIRECTION
## Using Pipes

### TRY IT - Using Pipelines

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
2. `wc --help `
- > Notice this line: 
```
"With no FILE, or when FILE is -, read standard input."
```
- > When a command can "read standard input" when no FILE is provided, this means you can ***pipe*** to that command.	
3. `cat /usr/share/dict/words `
- > Notice there are over 479,000 lines of output.
4. `wc -l /usr/share/dict/words `
5. `cat /usr/share/dict/words | wc -l `
- > Notice that the STDOUT of the `cat` command was read from STDIN by the command after the pipe.
6. `ll -R /tmp | wc -l `
- > Notice that STDERR goes to terminal while STDOUT goes to STDIN of the `wc` command.  
- > **STDERR must be handled before the pipe.**
7. `ll -R /tmp 2>/dev/null | wc -l `

![image](https://user-images.githubusercontent.com/36435980/144665382-d779d007-a656-4daa-bec2-49a31f0b12c2.png)
	
8. `find /usr/share/doc/ `
9. `find /usr/share/doc/ | grep 'readme' `
- > Notice only matches containing the string in quotes are shown.
10. `find /usr/share/doc/  | grep 'readme' | wc -l `
- > Counting the number of lines with `| wc -l` allows users to quickly see how many results the previous command returns.

![image](https://user-images.githubusercontent.com/36435980/144665859-2f3f6ff5-7a04-499e-93f3-85a728c21d73.png)

11. `find /usr/share/doc/  | grep --ignore-case  'readme' `
12. `find /usr/share/doc/  | grep --ignore-case  'readme' | wc -l  `
- > Notice there are many more matches for the string in quotes.

![image](https://user-images.githubusercontent.com/36435980/144666048-c903f5c3-0e5b-4ae0-959f-05991a74fb57.png)
	
13. `find /usr/share/doc/  | grep --ignore-case  'readme' | tee ~/readme_files.txt `
14. `wc -l ~/readme_files.txt `
- > Notice that STDOUT for `grep` is shown in the terminal and saved to a file when using the `tee` command.	
	
![image](https://user-images.githubusercontent.com/36435980/144666219-b2a4524b-5fec-417b-832f-77eab380aa32.png)
	
******
