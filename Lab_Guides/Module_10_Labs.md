# Configuring SSH (pages 108-115 & 443-452)
## SSH FEATURES (SSH/SCP/SFTP/RSYNC)

### TRY IT - SSH Basics

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh`
- > Note the usage example 
3. `ssh -<TAB x2> ` 
- > Note all the short options that work with **`<TAB>`** autocompletion

![image](https://user-images.githubusercontent.com/36435980/162841168-3816e496-de3f-401a-8d22-a5ce4f4d5d37.png)

4. `ssh -o <TAB x2>`
- > Note all the client options that work with **`<TAB>`** autocompletion after `-o`
- > View `man 1 ssh` for help with options

![image](https://user-images.githubusercontent.com/36435980/162841328-f9641885-4011-4b07-958b-10f92168c090.png)

5. `ssh -o P<TAB x2>`
- > Note the client options that begin with P will also autocomplete
- > Press **`<CTRL+u>`** to remove the partial command from the terminal or press **`<CTRL+c>`** to cancel the command but leave the text in the terminal
6. `which ssh`
7. `rpm -qf $(which ssh) `
8. `rpm -qd openssh-clients`

![image](https://user-images.githubusercontent.com/36435980/162841535-df27efee-d1d9-4b1a-a635-8c7843f81b22.png)

9. `ssh server1 'hostname ; whoami ; pwd' `
10. `ssh root@server1 'hostname ; whoami ; pwd' `

![image](https://user-images.githubusercontent.com/36435980/162843553-89e770c5-abab-4ee9-902b-9d003fceef4c.png)

******

# Configuring SSH (pages 108-115 & 443-452)
## USING SSH FOR SECURE FILE TRANSFER

### TRY IT - Using SFTP

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `sftp root@192.168.4.3`
3. Type the following commands at the `sftp> ` prompt
4. `pwd`
5. `lpwd`
6. `ls`
7. `lls`
8. `put /etc/hosts`
9. `ls`
10. `get anaconda-ks.cfg`
11. `lls`
12. `exit`

![image](https://user-images.githubusercontent.com/36435980/162843013-45ef497f-7d35-46e9-af38-bf0a448b9f76.png)


******

# Configuring SSH (pages 108-115 & 443-452)
## USING SSH FOR SECURE FILE TRANSFER

### TRY IT - Using SCP

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `scp`
- > Note the usage example
3. `scp -<TAB x2>`
- > Note the short options that work with autocompletion

![image](https://user-images.githubusercontent.com/36435980/162844013-a98edb8d-1d9c-47df-9050-0789ac21e0c2.png)

4. `scp -o<TAB x2>`
- > Note that `scp -o <OPTIONS>` uses the same ssh client options as `ssh -o <OPTIONS>`

![image](https://user-images.githubusercontent.com/36435980/162844127-01f61f9e-a738-47c5-ab75-ddb258dce772.png)

5. `scp -o P<TAB x2>`
6. `scp -o Pre<TAB>`
7. `scp -o PreferredAuthentications=<TAB x2>`
8. `scp -o PreferredAuthentications=password root@server2:/usr/share/dict/words  ~/words.txt`
9. `ll -h words.txt`
10. `scp  words.txt  student@server2:~/upload.txt`
11. `ssh student@server2 'ls -lh upload.txt ; wc -l upload.txt`   
- > Note that the copied file is the same size with a different name

![image](https://user-images.githubusercontent.com/36435980/162845470-fd9968e1-958a-49f0-8df4-f99c844236bb.png)

******

# Configuring SSH (pages 108-115 & 443-452)
## USING RSYNC FOR SECURE INCREMENTAL FILE TRANSFER

### TRY IT - Using RSYNC

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

# Configuring SSH (pages 108-115 & 443-452)
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

# Configuring SSH (pages 108-115 & 443-452)
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

# Configuring SSH (pages 108-115 & 443-452)
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

# Configuring SSH (pages 108-115 & 443-452)
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

# Configuring SSH (pages 108-115 & 443-452)
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

# Configuring SSH (pages 108-115 & 443-452)
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
