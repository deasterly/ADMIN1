# Using and Configuring SSH (pages 108-115 & 443-452)
## SSH FEATURES (SSH/SCP/SFTP/RSYNC)

### TRY IT - SSH Basics

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `ssh` client to run commands remotely
- Identify useful `ssh` client options
- Find documentation for the `ssh` client

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
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

# Using and Configuring SSH (pages 108-115 & 443-452)
## USING SSH FOR SECURE FILE TRANSFER

### TRY IT - Using SFTP

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `sftp` client to interactively transfer files  

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `sftp root@192.168.4.3`
3. Type the following commands at the `sftp> ` prompt
      1.  `pwd`
      2.  `lpwd`
      3.  `ls`
      4.  `lls`
      5.  `put /etc/hosts`
      6.  `ls`
      7.  `get anaconda-ks.cfg`
      8.  `lls`
      9.  `exit`

![image](https://user-images.githubusercontent.com/36435980/162843013-45ef497f-7d35-46e9-af38-bf0a448b9f76.png)

4. `rm -fv ~/anaconda-ks.cfg`

******

# Using and Configuring SSH (pages 108-115 & 443-452)
## USING SSH FOR SECURE FILE TRANSFER

### TRY IT - Using SCP

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `scp` client to transfer files

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `scp`
- > Note the usage example
3. `scp -<TAB x2>`
- > Note the short options that work with autocompletion

![image](https://user-images.githubusercontent.com/36435980/162844013-a98edb8d-1d9c-47df-9050-0789ac21e0c2.png)

4. `scp -o<TAB x2>`
- > Note that `scp -o <OPTIONS>` uses client options very similar to `ssh -o <OPTIONS>`

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

12. `rm -fv ~/words.txt`
13. `ssh root@server2 'rm -fv ~/upload.txt'  `


******

# Using and Configuring SSH (pages 108-115 & 443-452)
## USING RSYNC FOR SECURE INCREMENTAL FILE TRANSFER

### TRY IT - Using RSYNC

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `rsync` client for file transfer
- Use the `rsync` client for incremental file transfer

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `man rsync `
- > Review the SYNOPSIS section to see the syntax for `rsync` commands
- > Navigate to "OPTIONS SUMMARY" by typing a forward slash to search then type `/^OPTIONS<ENTER>`

![image](https://user-images.githubusercontent.com/36435980/162996846-326b1925-8cde-4b3b-b5f0-59e7b3105e52.png)

3. Review the **`-a, --archive`** option and note all the other options that a combined with `rsync -a`
- > **`-r`=recursive, '-l'=symlinks, `-p`=permissions, `-t`=timestamps, `-g`=group, `-o`=owner, `-D`=devices and special files** 

![image](https://user-images.githubusercontent.com/36435980/162998491-9e03c241-b560-49d4-9978-3c2236eee28e.png)

4. `mkdir -v /tmp/synctest`
5. `rsync -av  ~/  /tmp/synctest/ `

![image](https://user-images.githubusercontent.com/36435980/162999966-dd7dfde2-3d0b-47d1-a13e-40a53ecc68ff.png)
![image](https://user-images.githubusercontent.com/36435980/163000106-c319f464-be1c-4f1f-b8a5-bd951a12e66b.png)

- > Note the **`speedup is 1.00`** at the bottom of the `--verbose` output. This means 100% of the data had to be transferred so there was no speedup
6. `mkdir -v ~/newstuff`
7. `rsync -av  root@server1:/etc/   ~/newstuff/`

![image](https://user-images.githubusercontent.com/36435980/163001126-bdd8a31a-0820-46ea-8a34-cc02bcff2a09.png)
![image](https://user-images.githubusercontent.com/36435980/163001231-fa15849b-1ea0-4075-94c1-6983da4a4686.png)

8. `sudo rsync -av ~/  /tmp/synctest/`
- > Without `sudo` privileges some files in *~/newstuff/* from */etc/* on **server1** owned by **root** cannot be copied since `rsync -a` preserves ownership and permissions
- > Note the incremental transfer of only the newer data the second time the directories  */home/student/* and */tmp/synctest* are synchronized

![image](https://user-images.githubusercontent.com/36435980/163002643-c47ac4c4-d8e4-4489-93d9-ddd03295104c.png)
![image](https://user-images.githubusercontent.com/36435980/163002788-b3557502-1789-4678-a8ae-8281b42bedce.png)
 
 9. `rsync -av root@server1:/etc  ~/newstuff/`
 - > Note the ABSENCE of a trailing slash after ***server1:/etc*** and that when the source is a directory no trailing slash copies the directory itself while including the trailing slash includes only the contents and **not** the source directory

![image](https://user-images.githubusercontent.com/36435980/163004020-b4ee2bc9-b168-47f3-8fe6-83f5f2137bec.png)
![image](https://user-images.githubusercontent.com/36435980/163004281-2c29b87a-8ec4-4b9d-b623-1649f6308d1a.png)

10. `sudo rm -rf  /tmp/synctest  /home/student/newstuff `

![image](https://user-images.githubusercontent.com/36435980/163004750-12249c80-fe9e-4fd0-a8fe-3cf33f74d31f.png)

******

# Using and Configuring SSH (pages 108-115 & 443-452)
## LESSON REVIEW

### HANDS-ON EXERCISE - Using SSH Features

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use the `ssh` client to log in interactively
- Use the `ssh` client to run commands remotely 
- Use file transfer clients encrypted over SSH


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh root@server1`
- > Remember to include the **!** at the end of the root password --> **Passw0rd!** 
3. Type these commands in the terminal on **server1**:
      1. `ssh student@localhost 'hostname ; whoami' `
      2. `ssh server2 'hostname ; whoami' `
      3. `ssh student@server2 'hostname ; whoami' `
      4. `exit` 

![image](https://user-images.githubusercontent.com/36435980/165127216-5e6a09ab-0f75-42ca-9182-bbe86fcda2d9.png)

5. After returning to the terminal on **Workstation** as **student** type these commands in the terminal:
6. `mkdir ~/remote`
7. `scp root@server1:/etc/hosts  ~/remote/hosts.server1 `
- > Enter the **root** password when prompted
8. `scp root@server2:/etc/hosts  ~/remote/hosts.server2`
9. `ls -lh ~/remote/`
10. `cd ~/remote`

![image](https://user-images.githubusercontent.com/36435980/165127686-5200e91d-1c57-4c6e-88a3-e4cdac99abd8.png)

11. `rsync -av root@server1:/usr/share/info  ./ `
- > Enter the **root** password when prompted
12. `ls -ahl`

![image](https://user-images.githubusercontent.com/36435980/165128020-def96c16-d61c-497f-bc00-9fd15f0c4dad.png)
![image](https://user-images.githubusercontent.com/36435980/165128180-2064b3ae-630d-46ca-8581-d5415849d7ba.png)

13. `rsync -av root@server1:/usr/share/info/  ./  `

![image](https://user-images.githubusercontent.com/36435980/165128335-3a89f2ee-4949-4a5f-9d42-e8b2eb68e472.png)

14. `ls -hl`
- > Note that when using `rsync` only the contents are transferred if the source directory ends **with** a trailing slash, whereas the entire directory is transferred **without** the trailing slash.
15.  `cd `
16.  `rm -rf remote`

![image](https://user-images.githubusercontent.com/36435980/165128566-a1f51c57-713b-45c6-87fd-079c036e8e73.png)
![image](https://user-images.githubusercontent.com/36435980/165128701-a2b78094-1369-4863-b41e-d274023c2116.png)

******

# Configuring SSH (pages 108-115 & 443-452)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

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
2. ` `

******

# Configuring SSH (pages 108-115 & 443-452)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

> ### Perform the following tasks on the **Workstation VM** as user **student**.
******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. ` `

******

# Configuring SSH (pages 108-115 & 443-452)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

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
2. ` `

******

# Configuring SSH (pages 108-115 & 443-452)
## TOPIC TITLE | LESSON REVIEW | MODULE REVIEW

### TRY IT | HANDS-ON EXERCISE | END OF MODULE LAB - [Lab Title Here]

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
2. ` `

******
