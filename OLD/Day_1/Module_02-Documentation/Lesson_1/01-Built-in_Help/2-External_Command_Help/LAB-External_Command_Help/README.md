# DOCUMENTATION
## External Command Help

### TRY IT - External Command Help

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
