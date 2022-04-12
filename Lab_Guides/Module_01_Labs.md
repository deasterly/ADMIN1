# BASH Shell Basics 
## BASH Shell Features

### TRY IT - Working Efficiently in the Shell

> ### Perform the following tasks on the Workstation VM Console as user **student**.

******
### TASK 1: Log in to Workstation as user **student**
1. Log in to the Ubuntu Desktop as user **student** using **Passw0rd** for the password

![image](https://user-images.githubusercontent.com/36435980/143912652-69dda936-dea6-4e25-b755-0e0726291d78.png)

2. On the Ubuntu Desktop open Virtual Machine Manager 

![image](https://user-images.githubusercontent.com/36435980/143913153-b96fdd6d-4b46-4cae-b534-43be27eaabd9.png)

3. Launch the Workstation VM console
- > Unlock the screen if required

![image](https://user-images.githubusercontent.com/36435980/143913276-a0d1af48-d552-4bb2-9108-26de56493889.png)

4. Log in as **student** using **Passw0rd** for the password

![image](https://user-images.githubusercontent.com/36435980/143913326-b2e22bb0-8128-433b-a827-8498ac6eb620.png)

5. Open a Terminal

![image](https://user-images.githubusercontent.com/36435980/143913351-9bea6cd4-8fac-45af-83f2-295c7e145425.png)

******
### TASK 2: Type the following in the terminal: 
1. `ls <ENTER>`
2. `pwd <ENTER>`
3. `ls ; echo ; pwd <ENTER>`
- > Note that commands separated by **`;`** run sequentially.

![image](https://user-images.githubusercontent.com/36435980/143913599-c5b83c9d-49e4-48c8-bedc-14725867c600.png)

4. `ls --<TAB x2>` 
- > Notice that when there are multiple auto-complete options available, you must use **`<TAB>`** twice.

![image](https://user-images.githubusercontent.com/36435980/143913734-1527224e-af50-4eef-a1ce-c2040e331f1e.png)

5. `ls --v<TAB><ENTER>`  
- > Notice the option auto-completed with a single **`<TAB>`**.         
6. `ls --r<TAB x3>` 
- > Notice the letter **`e`** auto-completes after the first **`<TAB>`** then the full options appear after pressing **`<TAB>`** twice more.
  Choose to list the contents in reverse order by typing **`v<TAB><ENTER>`** or recursively by typing **`c<TAB><ENTER>`**.

![image](https://user-images.githubusercontent.com/36435980/143914307-90de27c2-5df8-4882-9094-58c18c261f8d.png)

7. `ls -ld  ~/D<TAB x2>`
- > Choose to list the *~/Desktop/* directory by typing **`e<TAB><ENTER>`** or continue choosing between *~/Documents/* and *~/Downloads/* by typing **`o<TAB x2>`** then typing either   **`c<TAB><ENTER>`** or **`w<TAB><ENTER>`**.

![image](https://user-images.githubusercontent.com/36435980/143914402-b97a0ba3-4008-4fd1-a065-2b196fba05de.png)

8. `ls<TAB x2>`
- > Notice many more commands start with `ls`.
9. `lsc<TAB><ENTER>`
- > View CPU information.
10. `lsb<TAB><ENTER>`
- > View storage block device information.
  Notice that auto-completion only requires a single **`<TAB>`** when there a no more ambiguous matches.
11. `<CTRL>+l`
- > Notice this clears the terminal like the command `clear`.
12. `<CTRL>+d`
- > Notice this logs the user out of their shell.

![image](https://user-images.githubusercontent.com/36435980/143914513-4fceef89-4542-442e-a31f-81a53723a4f4.png)

******

# USING THE BASH CLI SHELL
## BASH History

### TRY IT - Using BASH History

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
2. `help history `
- > Take a moment to read the help and take note of the HISTFILE location.	

![image](https://user-images.githubusercontent.com/36435980/144289557-802fc6d0-f714-4ac5-b721-92cd6fe7f537.png)

3. `history ` 
- > Use the up arrow to scroll through previous commands and notice they match the history output.

4. `!echo `
- > Notice this reprints the most recent line in the history starting with 'echo' and repeats the command.

5. `echo $(whoami) `
6. `!!<ENTER> `
- > Notice that typing '!!' will repeat the most recent command from the history.

7. `echo !1<ENTER> `
- > Notice this repeats the earliest command from your history.

8. `env | grep 'HIST' `
- > Notice that the maximum  size of the history and that duplicate commands are not repeated in the history.

9. `^HIST^HOST^<ENTER> `
- > Notice that you can perform history substitutions using the **'^'** character.

![image](https://user-images.githubusercontent.com/36435980/144289671-07f645b4-f9eb-45a0-9313-0bb4b2293892.png)


*****

# USING THE BASH CLI SHELL
## BASH Special Metacharacters

### TRY IT - Using BASH Metacharacters Correctly

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

# USING THE BASH CLI SHELL
## BASH Completion and Expansion

### TRY IT - Using BASH Shell Expansions

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Use Filename Expansion
1. Type these commands in the terminal: 
2. `man 7 glob `
- > Globbing is another name for **Filename Expansion**
- > Read the DESCRIPTION to the end of the "Ranges" section then press **`<q>`** to quit.

![image](https://user-images.githubusercontent.com/36435980/144292845-31523e9f-dea8-4073-8bca-d4c09323c4f5.png)

3. Practice using the following filename expansions (a.k.a. "globbing")
- `ls -ld D* `
- `ls -ld ?e* `
- `ls -ld ?o* `
- `ls -ld ?[oe]* `
- `ls -ld ?[^oe]* `
- `ls -ld ?[!oe]* `
	
![image](https://user-images.githubusercontent.com/36435980/144293392-7f128f3e-f4b1-4dff-9544-b4955d98f8e5.png)
	
### TASK 3: Use Command Substitution
1. Type these commands in the terminal: 
2. `man bash `
- > Type `/Command Substitution$<ENTER> ` then read to beginning of **"Arithmetic Expansion."**  Type **`<q>`** to quit when done.

![image](https://user-images.githubusercontent.com/36435980/144294073-08af8968-8680-44ca-818e-0c5a973c3ab0.png)

3. `echo  'whoami' versus `\` `whoami` \`
- > Notice that the second quotation marks are \` `backtick quotes` \` and not regular ` 'single quotes.' `

4. `echo "My working directory is $(pwd)." `
- > Notice there are two ways - \` `<commands>` \` and ` $(<commands>) ` -  to perform command substitutions.

![image](https://user-images.githubusercontent.com/36435980/144297134-c3bb8617-d2da-4263-8915-9457670fad8f.png)

### TASK 4: Use Tilde Expansion
1. Type these commands in the terminal: 
2. `man bash `
- > Type `/Tilde Expansion$<ENTER> ` then read the first paragraph.  Type **`<q>`** to quit when done.)

![image](https://user-images.githubusercontent.com/36435980/144297213-4c909eef-0150-4deb-ba60-96647aac8271.png)
	
3. `echo My user $USER has a home at ~ and root has a home at ~root `
- > Notice the tilde with no name expands to **$USER**'s home while **~NAME** expands to the home of **NAME**.
4. `echo "My user $USER has a home at ~ and root has a home at ~root " `
- > Notice that **tilde expansion does not work inside quotes**, even though variable/parameter expansion does.

	![image](https://user-images.githubusercontent.com/36435980/144297539-649d027d-9989-43cd-b631-cae1245c3e72.png)

### TASK 5: Use Brace Expansion
1. Type these commands in the terminal: 
2. `man bash `
- > Type `/Brace Expansion$<ENTER> ` then read the first 5 paragraphs.  Type **`<q>`** to quit when done.

![image](https://user-images.githubusercontent.com/36435980/144297830-2dd6bb5f-7c73-41c4-a36d-831fc164ed4a.png)

3. Practice using the following Brace Expansions
- `echo Example-{1..5} `
- `echo Example-{a,e,i,o,u} `
- `echo "Example-{1..5}" `
  - > Notice that **brace expansion does not work inside quotes**.

******

# USING THE BASH CLI SHELL (pages 38-39)
## Lesson Review

### HANDS-ON EXERCISE - BASH Shell Essentials

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Complete the following steps
1. Open the ***Pearson RHCSA 8 Cert Guide*** to page 38 
2. Complete **Exercise 2-3** from the book
3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 39
4. Complete **Exercise 2-4** from the book

******

# TYPES OF COMMANDS
## Shell Builtins

### TRY IT - BASH Builtins

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
2. `help | less ` 
- > Take a moment to read the top paragraph and list of built-in commands.

![image](https://user-images.githubusercontent.com/36435980/144315840-25f782be-217e-4d7c-bcf4-eaf4a5bafe67.png)

3. `rpm -ql bash | less `
- > Pay attention to all the files in */usr/bin/* that correspond to the BASH builtin commands

![image](https://user-images.githubusercontent.com/36435980/144316149-6a84def7-8da1-456e-a32a-8c80487ddf25.png)
	
4. `which cd `
5. `cat $(which cd) `
6. Review the `help` for the following builtin commands
- `help for `
- `help export `
- `help umask `

![image](https://user-images.githubusercontent.com/36435980/144316453-11000e03-6ed4-4e94-ac34-8c545c03aa5b.png)

*****

# TYPES OF COMMANDS
## External Commands

### TRY IT - Exernal Commands

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
2. `which cp `
3. `file $(which cp) `
- > Notice the output of `file` indicates this is a binary executable
4. `which zcat `
5. `file $(which zcat) `
- > Notice the output of `file` indicates this is a text executable script
6. `less $(which zcat) `

![image](https://user-images.githubusercontent.com/36435980/144317778-eb2b785f-569a-41df-b274-5b0dafe7e566.png)

******

# TYPES OF COMMANDS
## Aliases

### TRY IT - BASH Aliases

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Identify Aliases
1. Type these commands in the terminal: 
2. `which ll `
3. `alias -p `

![image](https://user-images.githubusercontent.com/36435980/144318636-7a8924c1-f99a-441b-98e5-a8fda0a62934.png)

4. `grep 'alias'  /etc/profile.d/*.sh `
- > Note that most aliases are defined by the BASH startup files. These will be covered in detail later.	

![image](https://user-images.githubusercontent.com/36435980/144318932-e1f28151-5b6b-4d8a-8b96-586afe6e8a57.png)

5. `sudo -i `
- > Enter ***Passw0rd*** when prompted.
6. `alias -p `
- > Notice that **root** has aliases for `mv` and `rm` that student does not have.
7. `exit `

![image](https://user-images.githubusercontent.com/36435980/144319179-4752c908-7dd1-4345-8983-c3b7aa95d785.png)

### TASK 3: Create Aliases 	
1. Type these commands in the terminal: 
2. `help alias `
- > Take a moment to read the help.
3. `labtest `
- > This will result in a **`"command not found"`** error, which is expected.
4. `alias labtest='echo Hello world' `
- > Note the use of single quotes and not backtick quotes after the `=` sign.
5. labtest

![image](https://user-images.githubusercontent.com/36435980/144319772-93f604f0-3bc9-4247-8b46-5ec5bab2fe29.png)

******

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

# USING THE BASH CLI SHELL
## MODULE REVIEW

### END OF MODULE LAB - Using the CLI

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******

### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.

******

### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

*****

### TASK 3:  Perform the following operations on SERVER2

1. Display only the first 10 lines of */usr/share/dict/words*
2. Display only the last 17 lines of */usr/share/dict/words*
3. Display the date in seconds since Jan 1st, 1970
4. Run the command that will show you the file type for */etc/group*
5. Run the command that will show you the absolute path to the command `uptime`
6. Determine what type of file is `uptime`
7. Show how many words are in the file */usr/share/dict/linux.words*
8. Create an alias called `utctime` that shows the time in UTC

*****

### SOLUTION

- > NOTE:  There may be many additional correct solutions other than those provided as examples in this guide.

1. Display only the first 10 lines of */usr/share/dict/words*

![image](https://user-images.githubusercontent.com/36435980/144328823-c5721147-f6a2-4294-8797-05db31502048.png)

2. Display only the last 17 lines of */usr/share/dict/words*

![image](https://user-images.githubusercontent.com/36435980/144328861-51b9d72c-1fb1-404c-810b-e3ee80a4bd1c.png)

3. Display the date in seconds since Jan 1st, 1970

![image](https://user-images.githubusercontent.com/36435980/144328897-3bf57e00-103d-47b3-8b1b-ad40b087822f.png)

4. Run the command that will show you the file type for */etc/group*

![image](https://user-images.githubusercontent.com/36435980/144328947-9ef42821-9fe0-42ee-a4d0-da7cbea248ac.png)

5. Run the command that will show you the absolute path to the command `uptime`

![image](https://user-images.githubusercontent.com/36435980/144328994-a74861d6-9642-41a9-aa49-fb80188750e6.png)

6. Determine what type of file is `uptime`

![image](https://user-images.githubusercontent.com/36435980/144329042-f25e814a-58bc-4908-a4b6-a8ddc9d8840d.png)

7. Show how many words are in the file */usr/share/dict/linux.words*

![image](https://user-images.githubusercontent.com/36435980/144329077-2f1eb0e2-3d12-4a19-a9e7-1076f0598179.png)

8. Create an alias called `utctime` that shows the time in UTC

![image](https://user-images.githubusercontent.com/36435980/144329118-6d9d006a-23f8-4087-addb-4c24bf12cec0.png)

******
