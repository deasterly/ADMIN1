# USING THE BASH CLI SHELL
## BASH Special Metacharacters

## TRY IT - Using BASH Metacharacters Correctly

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
2. `echo  $SHELL and  "$HOME" compared to  ;  echo   \$SHELL vs. '$HOME'  `

![image](https://user-images.githubusercontent.com/36435980/144291792-fcc2b43d-4311-497d-94de-062ffbb9fbcf.png)

- > Review the BASH info documentation for quoting and escaping by running `pinfo bash --node="Quoting" `

![image](https://user-images.githubusercontent.com/36435980/144291008-539396f8-3713-433c-9225-0151c5a1979e.png)

3. `ls /usr/share/doc `
- > Notice there are multiple lines of output.
4. `ls /usr/share/doc | less `
- > Notice piping the output to `| less` displays one page of output at a time. 
- > Press **`<h>`** for help and **`<q>`** to quit.
5. `ls /usr/share/doc | wc -l ` 
- > Notice piping the output to `| wc -l` reports how many lines the command sends to STDOUT.
6. `ls /usr/share/doc | grep cat `
- > Notice piping the output to `| grep <STRING> ` only displays matches for the search string.
	
![image](https://user-images.githubusercontent.com/36435980/144291910-be9c4525-2553-4ce8-8816-0efec557b972.png)

******
