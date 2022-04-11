# USING THE BASH CLI SHELL
## BASH History

## TRY IT - Using BASH History

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
