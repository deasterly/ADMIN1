# USING THE BASH CLI SHELL
## BASH Completion and Expansion

## TRY IT - Using BASH Shell Expansions

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
