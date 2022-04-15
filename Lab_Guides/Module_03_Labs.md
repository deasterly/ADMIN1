# THE VIM EDITOR
## Mode Based Operation

### TRY IT - Editing Text Files Using `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use `vimtutor` to learn how to use the `vim` editor

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
2. `vimtutor `
- Make sure the **`<CAPSLOCK>`** key is off
- Press **`<j>`** until you can see all of **"Lesson 1.1: MOVING THE CURSOR"** in the terminal.
  - Practice using the navigation keystrokes covered in **"Lesson 1.1"** until you have committed them to memory
- Use **`<j>`** to scroll down to **"Lesson 1.2."**
3. Before performing the steps in **"Lesson 1.2: EXITING VIM"** do the following tasks:
- Press **`<ESC>`** to make sure VIM is in Command Mode, a.k.a. Normal Mode.
- Type `:w ~/myvimfile.txt<ENTER> `
- > This saves the file in your home directory for later.
4. After completing step 2 of **"Lesson 1.2"** type ` vim ~/myvimfile.txt ` then resume **"Lesson 1.2"** after step 3.
- Continue the lessons down to the end of "Lesson 1.5."
- Adapt the commands in **"Lesson 1.6"** to use *~/myvimfile.txt* and read to the end of **"Lesson 1 SUMMARY."** 
5. Save your file and exit the editor.



https://user-images.githubusercontent.com/36435980/144520039-7b34ce90-987e-4478-b54b-2efce9353ac3.mp4


******
# THE VIM EDITOR
## EX Mode (Extended Command Mode) Basics

### TRY IT - Saving and Exiting in `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use Extended Command Mode, a.k.a. **"EX Mode"** in `vim`

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
2. `ls -lh > files.txt `
3. `vim files.txt `
4. Perform the following tasks in the editor:
- Press **`<ESC>`** to confirm the editor is in Command Mode.
- Type `:help<ENTER>` to view the EX Mode help
- Type `<ESC>:q<ENTER>` to leave the help and return to *files.txt*
- Type `<ESC>:help quit<ENTER>` and read down to the `ZQ` command, stopping at "MULTIPLE WINDOWS AND BUFFERS" 
5. Quit the editor without saving.


******
# THE VIM EDITOR
## Visual Mode Selection for Copying and Pasting

## TRY IT - Selecting, Copying, and Pasting in `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use `vim` features for navigation, selection, deletion, copying, pasting, and repetition 
- Use `vim` EX Mode for file operations and to enable/disable line numbers

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
2. `ls -ahl > homedir.txt `
3. `vim ~/homedir.txt `
- Perform the following tasks in the editor:
4. With the cursor at **position 1,1** type **`dd`** to delete the first line.
- > Confirm your cursor position using the lower right corner of the editor window.
5. Type **`u`** to ***undo*** the change.
6. Type **`<CTRL>+r`** to ***redo*** the undone change.
7. Type **`5j`** to ***jump down*** five lines to **position 6,1**.
8. Type **`$`** to move to the end of line 6.
9. Type **`v`** to switch to **VISUAL** mode.
- > Confirm you are in VISUAL mode using the prompt in the lower left corner of the editor window.
10. Type **`gg`** to ***go*** back to **position 1,1** at the top of the document.
11. Type **`y`** to ***yank*** a copy of the selected lines and notice the prompt message.
12. Type **`<SHIFT>+P`** to ***put*** the yanked lines above the first line and notice the prompt message.
13. Type **`<ESC>:set number`** to turn on line numbers.
14. Type **`<SHIFT>+V`** to switch to **VISUAL LINE** mode and notice all of line 1 is highlighted.
15. Type **`j`** until the line for the directory *Desktop/* is highlighted.
16. Type **`r0`** to ***replace*** all the selected lines with zeros.
17. Type **`u`** to ***undo*** the previous replace operation.
18. Make sure the cursor is at **position 1,1**.
19. Type **`<SHIFT>+V`** to switch to **VISUAL LINE** mode and notice all of line 1 is highlighted.
- > Confirm you are in VISUAL LINE mode using the prompt in the lower left corner of the editor window.
20. Type **`12j`** to select the first thirteen lines.
21. Type **`x`** to ***cut*** the selected line.
22. Type **`<SHIFT>+G`** to go to the last line.
23. Type **`<ESC>:set nonumber`** to turn off line numbers.
24. Type **`dd`** to ***delete*** the last line.
25. Type **`yy`** to ***yank*** a copy of the new last line.
26. Type **`3p`** to ***put*** 3 copies of the yanked line at the bottom and notice the prompt message.
27. Type **`.`** (a dot/period) to ***repeat the last operation***.
28. Save the edited file as *~/homedir2.txt* and discard changes to the original file.
- Type **` <ESC>:wq!  ~/homedir2.txt `**



https://user-images.githubusercontent.com/36435980/144653014-189997f4-4fd5-4dea-883e-94dc7e2f2fec.mp4


******
# THE VIM EDITOR
## Lesson Review

### HANDS ON EXERCISE - Create and Edit Text Files Using `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `vim` editor and its many features

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
3. Type the following in the SSH terminal on server1
4. `tail -n15 /usr/share/dict/words > myfile `
5. `cat myfile `
6. `less myfile `
7. While viewing *myfile* in `less`, press **`<v>`**.
- > Note that pressing **`<v>`** when reading a text file with `less` will open the file in `vim`.
8. Perform the following operations in VIM:
9. Press **`<ESC>`** then type **`<SHIFT>+<:>`** to ensure VIM is in **EX/Extended Command** mode.
10. Type **`set number`** at the EX mode prompt to turn on line numbers.
11. Press **`<gg>`** to make sure the cursor is in **position 1,1**.
12. Type **`<3yy>`** to yank a copy of the next 3 lines.
13. Type **`<2p>`** to paste 6 more lines into the file.
14.	Press **`<k>`** to move the cursor back to **position 1,1**.
15. Press **`<yy>`** to yank a copy of the top line.
16. Press **`<SHIFT>+<G>`** to go to the bottom line.
17.	Type **`<4p>`** to paste 4 more lines into the file.
18.	Type **`<3dd>`** to remove all but one of the pasted lines.
19.	Press **`<u>`** to undo the most recent change .
20.	Press **`<ESC>`** to ensure VIM is in Normal/Command mode.
21. Type **`<SHIFT>+<:>`** to switch to EX/Extended Command mode.
22. Type **`9<ENTER>`** move to line 9 from the EX mode prompt.
23.	Press **`<SHIFT>+<V>`** to switch VIM to **VISUAL LINE** mode.
24.	Type **`<5k>`** to select and highlight 5 more lines.
25.	Press **`<~>`** to change the case of the selection.
26. Type **`<gg>`** to move the cursor to **position 1,1**.
27. Press **`<CTRL>+<v>`** to switch VIM to **VISUAL BLOCK** mode.
28. Press **`<SHIFT>+<G>`** to go to the bottom line and select the first column.
29. Press **`<y>`** to yank a copy of the first column.
30. Press **`<SHIFT>+<P>`** to paste a new first column.
31. Type **`<3.>`** to repeat the last Normal/Command mode operation 3 times.
32. Press **`<SHIFT>+<G>`** to move the cursor to the last line.
33. Press **`<SHIFT>+<O>`** to open a new line in Insert mode.
34. Type in "this is some new text "
```
this is some new text
```
35.	Press **`<ESC>`** to return to Normal/Command mode.
36.	Press **`<SHIFT>+<G>`** to move the cursor to the last line again.
37.	Press **`<ESC>`** then type **`<SHIFT>+<:>`** to switch to EX mode.
38.	Type **`r  !  ls -lah `** at the EX mode prompt to insert the output of `ls -lah` at the cursor location .
39. Press **`<ESC>`** then type **`<SHIFT>+<:>`** to switch to EX mode.
40.	Type **`wq`** at the EX mode prompt to write and quit VIM returning to the earlier `less` command.
41. Press **`<q>`** to quit the `less` text pager.


https://user-images.githubusercontent.com/36435980/144658535-05020914-b121-4c24-83ff-f12274a9589d.mp4

******
# INPUT/OUTPUT REDIRECTION
## Redirection Symbols and I/O Streams

### TRY IT - Redirecting STDOUT and STDERR

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use BASH shell redirection metacharacters correctly
- Redirect STDOUT and STDERR using their file descriptor numbers


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
8. `ll -R /tmp 2>  ~/tmpfiles1.txt `
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
# INPUT/OUTPUT REDIRECTION
## Using Pipes

### TRY IT - Using Pipelines

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the pipe symbol ( `|` ) to redirect the output (STDOUT) from a command to the input (STDIN) of another comand

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
# INPUT/OUTPUT REDIRECTION
## Lesson Review

### HANDS ON EXERCISE - Using I/O Redirection and Pipelines

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the pipe symbol ( `|` ) to redirect the output (STDOUT) from a command to the input (STDIN) of another comand
- Use the `tee` command

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~USER** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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
# WORKING WITH TEXT
## Module Review

### END OF MODULE LAB - Working with Text

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Edit text
- Use I/O redirection

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
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

1. Put the first 15 lines of the file */usr/share/dict/words* into the file *~/myfile*.
2. Remove any lines that end in numbers from *~/myfile*.
3. Change all lower case letters in *~/myfile* to capital letters and change the only capital letter to lower case.
4. Find all of the **pdf** files in the file system and list the locations in a text file named *~/pdf.lst*.
5. Find all of the **jpg** files in the file system and list the locations in a text file named *~/jpg.lst*
6. Create a file that reads "Welcome to Server 2" named *welcome.txt* in */etc/skel/* 

*****
### SOLUTION


1. Put the first 15 lines of the file */usr/share/dict/words* into the file *~/myfile*.

![image](https://user-images.githubusercontent.com/36435980/144685150-24368165-a03e-459a-80c2-29be7ece9cc8.png)

2. Remove any lines that end in numbers from *~/myfile*.
3. Change all lower case letters in *~/myfile* to capital letters and change the only capital letter to lower case.
- > The tilde key (**`<SHIFT + ~>`**) changes the case of selected text in Command Mode.

![image](https://user-images.githubusercontent.com/36435980/144685214-7de9a856-0ccb-4846-ba7d-0a31267f06b5.png)

4. Find all of the **pdf** files in the file system and list the locations in a text file named *~/pdf.lst*.

![image](https://user-images.githubusercontent.com/36435980/144685249-30c2f6ec-5520-4c00-914e-6f4bb50b0154.png)

5. Find all of the **jpg** files in the file system and list the locations in a text file named *~/jpg.lst*

![image](https://user-images.githubusercontent.com/36435980/144685280-89183029-60ac-4fb5-bc29-dc10f75104e4.png)

6. Create a file that reads "Welcome to Server 2" named *welcome.txt* in */etc/skel/* 

![image](https://user-images.githubusercontent.com/36435980/144685340-a0ad88d1-a856-4ddb-b481-23ae412fe0eb.png)

******
