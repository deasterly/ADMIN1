# DOCUMENTATION
## Bultin-in Help

### TRY IT - BASH Builtins Help

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use BASH shell builtins documentation from manuals, info docs, and the builtin `help` command

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
2. `pinfo bash `
- Navigate to the **" * Shell Builtin Commands:: "** node and press **`<ENTER>`**
- Read the first 4 paragraphs and press **`<q>`** to quit when done.
  - According to the 3rd paragraph, there are 4 groups of builtin commands that have their own documentation chapters.
- > QUESTION: What functionality do these 4 groups of builtins provide the shell?

![image](https://user-images.githubusercontent.com/36435980/144467137-88e35a0a-4ef4-4f7a-9625-8eaffb1ea17f.png)

5. `man builtins `
- > Review the list of commands in the **NAME** section of the manual that are provided as part of the shell.

![image](https://user-images.githubusercontent.com/36435980/144468391-610e487b-043f-424d-85c7-ce5572c4c07f.png)

6. `help | less `
- > DISCUSSION QUESTION: Which of the commands listed with `help` do you use most often?

******
# DOCUMENTATION
## External Command Help

### TRY IT - External Command Help

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the native help option(s) for external commands
- Search for specific help topics using `COMMAND --help | grep 'SEARCHSTRING' ` 

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
2. `mkdir --help `
- > Notice that 'Usage:' is first, followed by the default behavior of the command. 

![image](https://user-images.githubusercontent.com/36435980/144483692-7de3df31-c51d-4927-aa13-0ec88f559af6.png)

- > Full documentation is referenced at the bottom.
3. `ls --help `
- > Notice there are multiple lines of output. Scroll up in the terminal with **`<SHIFT+PG_UP>`** as needed.
4. `ls --help | less `
- > Notice that reading `--help` output through ` | less` allows searching for text and quick navigation.
5. `tar --help | head `
- > This displays just the first 10 lines of help.

![image](https://user-images.githubusercontent.com/36435980/144485101-f9fae642-8e64-4d25-abdb-4841a4ef540e.png)

6. `ls --help | grep 'sort' `
7. `grep --help | grep -i 'case' `
- > Using ` --help | grep 'string' ` displays any lines of help containing the string in single quotes.

![image](https://user-images.githubusercontent.com/36435980/144485255-68c970fa-6366-4c71-9459-47535d9b3afb.png)

******
# MANUALS
## Reading Manuals

### TRY IT - Reading Manual Pages

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `man` command to read documentation

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
2. `man man `
- Take a few moments to read the **DESCRIPTION** and **EXAMPLE** sections of the manual.

![image](https://user-images.githubusercontent.com/36435980/144487597-7b4402d4-49a6-4e48-9263-23a026084e26.png)
![image](https://user-images.githubusercontent.com/36435980/144487734-0051f173-fd38-475d-99ee-49d5b577cfe2.png)
![image](https://user-images.githubusercontent.com/36435980/144487794-97135955-f6c4-4149-9295-1df29e0cc615.png)

- After completing the **EXAMPLE** section, press **`<h>`** for help searching and navigating the manual.

![image](https://user-images.githubusercontent.com/36435980/144487891-80171535-cc37-46a4-b48b-22294652b03c.png)

- Press **`<q>`** to return to the manual.
- Next press the slash key **`</>`** to start a text search.
- Type `mode<ENTER>` in the search prompt to find the "Main modes of operation" section of the manual.

![image](https://user-images.githubusercontent.com/36435980/144488798-a8ed61ab-9579-4499-bc39-64f8d096150d.png)

- Refer to this section to understand the options in the **SYNOPSIS** section of the manual.
- Press **`<g>`** twice to go to the top of the manual and review the **SYNOPSIS** then press **`<q>`** to quit.

![image](https://user-images.githubusercontent.com/36435980/144489306-a73da60c-0622-4d2f-981d-e2554583bfe2.png)

3. `man -f intro `
4. `man -a intro `
- > Review the "intro" page for each section number.

![image](https://user-images.githubusercontent.com/36435980/144489466-b66e8d5f-d1c4-4acb-b49c-dce8b3661e70.png)

******
# MANUALS
## Searching Manuals

### TRY IT - Searching the Manual Database

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `man` and its options to search the manuals
- Use the `apropos` and `whatis` commands to search manual database
- Use the `mandb` command to update the manual database

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Search manual pages
1. Type these commands in the terminal: 
2. `sudo mandb `
- > Enter ***Passw0rd*** when prompted.
3. `man -k manual `
- > Note that `man -k STRING ` searches for STRING in the **TITLE** and **NAME** sections of the manual pages.
4. `man -f passwd `
- > Note that `man -f STRING ` searches for STRING only in the **TITLE** section of the manual pages.
5. `whatis passwd `
- > Note that `whatis` and `man -f` are synonymous.

![image](https://user-images.githubusercontent.com/36435980/144491599-cdf94885-c5ae-459b-a45a-526294322d4f.png)

6. `man -k regex `
7. `apropos regex `
- > Note that `apropos` and `man -k` are synonymous.

![image](https://user-images.githubusercontent.com/36435980/144491510-7e180740-8162-4c84-b052-bfcf9ddf9216.png)

8. `man -K dell.com `
- > Use `less` searching - remember **`<h>`** for help - to find the matching text in the open manual.

![image](https://user-images.githubusercontent.com/36435980/144491459-93c48d85-911e-4d52-b466-4939789485c1.png)

9. `man -K dell `
- > Find the matching text in two or more manuals. 

![image](https://user-images.githubusercontent.com/36435980/144491312-ffaf9c42-37a9-4060-81f2-50f8a58e413a.png)

- > Skip results with **`<CTRL+d>`** and quit with **`<CTRL+c>`** after you have mastered searching manuals.

******
# GNU INFO
## Reading Info Docs

### TRY IT - Using GNU Info Documentation and `pinfo`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the commands `pinfo` and `info` to view documentation from the GNU Project

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Read and understand GNU INFO documentation
1. Type these commands in the terminal: 
2. `whereis pinfo `
3. `ls /usr/share/info `

![image](https://user-images.githubusercontent.com/36435980/144492624-b283b8da-c4b5-42c2-a21c-c1497691d9cd.png)

4. `pinfo  <TAB x2> `
5. `pinfo core<TAB><ENTER> `
- > Take a moment to read through the list of menu items, using the arrow keys or **`<j>`** to scroll down. 

![image](https://user-images.githubusercontent.com/36435980/144492874-e3e10118-4049-4edf-86ef-d1aaec3d1498.png)
![image](https://user-images.githubusercontent.com/36435980/144492937-ade91fed-d725-485b-b89d-b5de1ed81b7c.png)

- > Then press **`<q>`** to quit.
6. `pinfo coreutils --node="Basic operations" `
- > Take a moment to read the navigation guide at the top. 
- Press **`<n>`** to go to the next node. 
- Next press **`<u>`** to go up to the top node. 

![image](https://user-images.githubusercontent.com/36435980/144493410-9b0978ab-218a-4205-aa49-9829ac2536c6.png)

- Then press **`<q>`** to quit.)
7. `info `
- > The `pinfo` viewer may not be present on all systems. When that is the case use the `info` viewer instead. 

![image](https://user-images.githubusercontent.com/36435980/144493772-addd255b-5524-479b-afa2-737bdb3ea32e.png)

- Press **`<h>`** to view the tutorial and **`<SHIFT+H>`** to view the command keys for `info` then press **`<q>`** to quit.
	
![image](https://user-images.githubusercontent.com/36435980/144493827-ecc3aa48-caaf-43c8-820b-809d293b450b.png)
![image](https://user-images.githubusercontent.com/36435980/144493871-01dd2b47-f630-4cfc-9ad1-ea67fc3036c5.png)
	
******
# Documentation
## Lesson Review

### HANDS ON EXERCISE - Searching and Using Documentation

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Search documentation
- Read documentation

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
4. `man apropos ` 
- > Read the **DESCRIPTION** and **SEE ALSO** sections of the manual.
5. `man -k mandb `
6. `man mandb `
7. `mandb `
- > Note that user **student** does not have permission to update the manual search index.

![image](https://user-images.githubusercontent.com/36435980/144495199-d663bb92-97f0-40aa-b652-4388bdf5292d.png)

8. `sudo mandb `

![image](https://user-images.githubusercontent.com/36435980/144495290-7ffd921c-3174-44b1-8b8e-202385916c26.png)

9. `man -k mandb manuals documentation `

![image](https://user-images.githubusercontent.com/36435980/144495381-8a408d06-b6a8-43e9-8206-3c573c1f2f1f.png)

10. `man -f passwd `
11. `whatis passwd `
12. `man 5 passwd `
- > Notice section 5 covers configuration files.
13. `man 1 passwd `
- > Notice section 1 covers commands.
14. `man -K passwd `

![image](https://user-images.githubusercontent.com/36435980/144495791-c4b2acf3-425a-487e-9b53-c7f1f49ae281.png)

15. `pinfo pinfo `
- > If you want to fully understand all the keybindings in `pinfo` take a look at the "Configuration file," "Example config file" and "Keybindings" nodes.

![image](https://user-images.githubusercontent.com/36435980/144496339-146c3c00-3534-4ed3-8b3b-7755f4f23eb4.png)

16. `pinfo bash `
- Navigate to the **" \* Introduction::"** node.
![image](https://user-images.githubusercontent.com/36435980/144496516-a5a1ca57-b0e9-470c-b041-dfeb028b9b10.png)

- Read the "What is Bash?" and "What is a shell?" nodes.)
![image](https://user-images.githubusercontent.com/36435980/144496571-9a559d63-e598-4352-aaf0-d0645bed1194.png)

******
# DOCUMENTATION
## Module Review

### END OF MODULE LAB - Help and Documentation

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Search documentation
- Read documentation

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

1. Update the manual page database.
2. Find out where the command `find` will execute from **and** where to find documentation in a single command.
3. Locate anything in the directory */usr/share/doc* with **README** in the name.
4. Use the manual for the `find` command and locate an **EXAMPLE** showing how to execute a command on each result found.
5. Use  ***coreutils.info*** to look up how use use the `cut` command to separate lines of text into fields.
- > Find the default *delimiter* for separating fields and the option to **override** the field delimiter.

*****

### SOLUTION

- > NOTE:  There may be many additional correct solutions other than those provided as examples in this guide.

1. Update the manual page database.

![image](https://user-images.githubusercontent.com/36435980/144499593-f17db39f-f47f-4b67-9bb8-7dcc6d070cf4.png)

2. Find out where the command `find` will execute from **and** where to find documentation in a single command.

![image](https://user-images.githubusercontent.com/36435980/144499711-1be19f8f-9629-4ff0-8055-5df83570a821.png)

3. Locate anything in the directory */usr/share/doc* with **README** in the name.

![image](https://user-images.githubusercontent.com/36435980/144499396-90e829e7-e8f9-4ea7-a492-e5d811a2c667.png)

4. Use the manual for the `find` command and locate an **EXAMPLE** showing how to execute a command on each result found.

![image](https://user-images.githubusercontent.com/36435980/144504730-045e3a67-fb62-4c69-b579-e18269a9160c.png)

5. Use  ***coreutils.info*** to look up how use use the `cut` command to separate lines of text into fields.
- > Find the default *delimiter* for separating fields and the option to **override** the field delimiter.

![image](https://user-images.githubusercontent.com/36435980/144517084-1b6beaa2-8562-482d-9f1a-295ddcb8f1c8.png)

******
