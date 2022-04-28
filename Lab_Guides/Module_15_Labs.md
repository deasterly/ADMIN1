# BASIC STORAGE (pages 309-335)
## PARTITIONS

### TRY IT - Identifying Block Devices and Filesystems

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## PARTITIONS

### TRY IT - MBR Partitioning Using `fdisk`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## PARTITIONS

### TRY IT - GPT Partitioning Using `gdisk`


> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## PARTITIONS

### TRY IT - GNU `parted` Documentation

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## LESSON REVIEW 

### HANDS-ON EXERCISE - Creating Partitions

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## CREATING AND MOUNTING FILESYSTEMS

### TRY IT - Create and Mount XFS Filesystems

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## CREATING AND MOUNTING FILESYSTEMS

### TRY IT - Create and Activate Swap Filesystems

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## CREATING AND MOUNTING FILESYSTEMS

### TRY IT - Using */etc/fstab* to Make Mounts and Swaps Persistent  

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## LESSON REVIEW

### HANDS-ON EXERCISE - Persistently Mount a New Partition

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# BASIC STORAGE (pages 309-335)
## MODULE REVIEW

### END OF MODULE LAB - Basic Storage

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Task 1
- Task 2
- Task 3


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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
