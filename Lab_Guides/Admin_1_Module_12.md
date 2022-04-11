# LESSON TITLE (pages xx-yy)
## TOPIC TITLE

## LAB TITLE

> ### Perform the following tasks on the **HOST** as user **USERNAME**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~USER** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `echo "Enter commands and keystrokes between backticks in MarkDown."  `
- > Note that commands can be explained with an UL indented blockquote
3. `echo "Keystrokes should be enclosed in backtick quotes AND tagged with angle brackets like <TAB x2>"  ` 
- > Keystrokes in notes should be made **bold** then backtick enclosed like **`<CTRL+ALT+DEL>`** 
4. Add the following text to the file */etc/sudoers.d/demo*
```
instructor  ALL=(ALL)    NOPASSWD:  ALL
```
- > Use I/O redirection or `vim /etc/sudoers.d/demo` as preferred
- > File paths in notes should be italic like *~/Desktop/* but not inside backtick-enclosed commands
- > Text edits and script examples should be preceded and followed by triple backticks on the surrounding lines
- > The HTML tags `<PRE>` and `</PRE>` might also work to ensure proper spacing and formatting
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

