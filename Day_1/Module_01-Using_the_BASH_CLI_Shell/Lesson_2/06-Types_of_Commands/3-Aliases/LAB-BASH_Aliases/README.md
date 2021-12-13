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
