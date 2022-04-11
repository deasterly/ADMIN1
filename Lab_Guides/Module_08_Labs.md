# PROCESS BASICS (pages 233-251)
## MANAGING PROCESSES

### TRY IT - Job Control

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `sudo -i `
- > Confirm you are now user **root** on **Workstation**
3. Review documentation from these commands:
    1) `help jobs`
    2) `help bg`
    3) `help fg`
3. Open the ***Pearons RHCSA Cert Guide*** to page 238
4. Complete ##Exercise 10-1** from the book

******

# SIGNALS (pages 239-242, 244-248)
## SENDING SIGNALS TO PROCESSES

### TRY IT - Sending Signals to Processes

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Read pages 244-245 of the ***Pearson RHCSA Cert Guide***
2. Type these commands in the terminal: 
    1) `sleep 10000 `
    2) Press **`<CTRL+c>`** to interrupt the process
    3) `sleep 10000 &`
    - > Run this command 2 more times to have 3 jobs running in the background
    4) `jobs`
    5) `fg 1`
    - > Bring the first `sleep` job to the foreground
    6) Press **`<CTRL+z>`** to stop the foreground job
    7) `bg 1`
    - > Return the stopped job to running in the background
    8) `jobs`
    9) `pgrep sleep`
    - > Take note of the PIDs listed referenced as (PID1)-(PID3) in upcoming commands
    10) `kill -l`
    - > Notice the different signals that can be sent to processes by `kill`
    11) `kill -9 (PID3)`
    12) `kill -SIGINT (PID2)`
    - > Pay attention to the difference in the output of the last 2 commands
    13) `killall -TERM sleep`
    14) `jobs`

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******

# LESSON TITLE (pages XX-YY)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
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
5. Create the following users with the provided group memberships and account settings
- > When creating users, groups, shares, etc. make requirements easy to understand with tables

| LOGIN   | GECOS    | SHELL    | UID#    | GROUPS    | UMASK |
| :------ | :------- | :------- | :-----: | :-------- | :---: |
| bob | Robert Smith | /bin/bash | 2001 |wheel | 027 |
| joe | Jo Evans | /bin/bash | 2002 | cdrom, wheel | 022 |

******
