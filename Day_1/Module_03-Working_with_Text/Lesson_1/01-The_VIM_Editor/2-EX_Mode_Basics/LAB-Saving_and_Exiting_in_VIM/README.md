# THE VIM EDITOR
## EX Mode (Extended Command Mode) Basics

### TRY IT - Saving and Exiting in `vim`

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
2. `ls -lh > files.txt `
3. `vim files.txt `
4. Perform the following tasks in the editor:
- Press **`<ESC>`** to confirm the editor is in Command Mode.
- Type `:help<ENTER>` to view the EX Mode help
- Type `<ESC>:q<ENTER>` to leave the help and return to *files.txt*
- Type `<ESC>:help quit<ENTER>` and read down to the `ZQ` command, stopping at "MULTIPLE WINDOWS AND BUFFERS" 
5. Quit the editor without saving.


******
