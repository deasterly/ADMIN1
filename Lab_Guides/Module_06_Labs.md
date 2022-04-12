# LOCAL USERS AND GROUPS
## Group Management

### TRY IT - Managing Local Groups

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `groupadd --help  `
3. `sudo groupadd group1 `
4. `getent group  | tail -n 3 `
- > Note that the new group was added to the end of the file */etc/group* and took the next unused GID number.

![image](https://user-images.githubusercontent.com/36435980/145646755-616b55a1-a759-403d-b959-09ba5cb620d9.png)

5. `sudo groupadd --gid 2000  group2 `
6. `getent group  | grep  'group'  `
7. `groupmod --help `

![image](https://user-images.githubusercontent.com/36435980/145647155-e77e3175-d83c-4ada-ad2a-1a494559c912.png)

8. `sudo groupdel  group1 `
9. `getent  group  | grep 'group'  `
- > Only **group2** with the GID of 2000 remains.
10. `groupmod  --gid  5000   --new-name group0   group2 `
11. `getent group | grep 'group'  `
- > Note that both the name and GID of the group were changed. 

![image](https://user-images.githubusercontent.com/36435980/145647647-8a11ebeb-8263-40da-8e21-31fd5f431617.png)

*****
# LOCAL USERS AND GROUPS
## User Management

### TRY IT - Managing Local Users

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
2. `grep 'student'  /etc/passwd  /etc/group  `
3. `id student `
4. `useradd --help | less `
- > Notice the options for setting the UID number, GECOS comment, home directory, shell, and group memberships with `useradd`.
5. `sudo useradd user1`
6. `sudo useradd -u 3002 -c "Test User 2" user2  `
7. `sudo useradd -G cdrom,wheel,group0  -c "Test User 3"  user3 ` 
8. `grep  'user[0-9]'  /etc/passwd   /etc/group ` 

![image](https://user-images.githubusercontent.com/36435980/145649290-6556e76a-5ad5-41ca-b39c-8f56314a3867.png)

9. `usermod --help | less `
- > Notice that most options for `useradd` and `usermod` are similar.  
10. `sudo usermod --comment "Test User 1" --groups group0  user1 `
11. `getent passwd user1 `
12. `sudo usermod --uid 3001  user1  `
13. `grep 'user1'  /etc/passwd   /etc/group  `

![image](https://user-images.githubusercontent.com/36435980/145650351-5a8cbcd8-03e7-4aad-8df8-98e3fb3eccdd.png)

14. `ls /home `
- Notice the home directories for the 3 test users.
15. `sudo find  /   -user  user3  2>  /dev/null `
- > This finds all files belonging to **user3**  while ` 2>  /dev/null ` discards errors such as "Permission denied."
16. `sudo userdel  -r  user3 `
17. `sudo find  /  -user  user3 `
18. `ls /home `
- > Notice that the account for **user3** no longer exists. 

![image](https://user-images.githubusercontent.com/36435980/145651650-f6f13cd5-8b0f-43d9-be98-8d3f8f74209e.png)

19. `sudo passwd user1 `
- > Set the password to **Passw0rd** when prompted.
20. `sudo -i `
- > Only an administrator can set another user's password.
21. `echo  Passw0rd | passwd --stdin  user2 ` 
- > Notice this method allows passwords to be set without typing them twice.
22. `exit `

![image](https://user-images.githubusercontent.com/36435980/145652699-72950846-ad72-4a71-9c4c-d0a63ce3225e.png)

23. `ssh user1@localhost`
- > Enter the password set in a previous step.
24. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the **Workstation VM** and are working the the ***~user1*** home directory.
25. `passwd `
- > Change the password for **user1** to a more secure password of your choice (**PassTheEX200!!** for example).
- > Pay attention to the prompts!  Users must enter their CURRENT password before entering the new password with `passwd`.
26. `exit `
27. `ssh user1@localhost `
- > Confirm the new password for **user1** works correctly.

![image](https://user-images.githubusercontent.com/36435980/145652872-e3adf68c-c6f1-4668-b2d4-2b955b6cf153.png)

*****
# MANAGING USERS
## Lesson Review

### HANDS ON EXERCISE - Managing Local Users and Groups

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `sudo -i`
- > Enter **Passw0rd** when prompted.
5. `hostname ; whoami ; pwd `
- > Confirm you are logged in to **SERVER1** and are starting from the ***~root*** home directory.

![image](https://user-images.githubusercontent.com/36435980/145691243-11921e9a-9f31-468b-92e8-e44721ac1ec0.png)

*****
### TASK 3: Create the following groups and users

| GROUP NAME | GID# |
| :--------- | :--: |
| database   | 200  |
| dbadmin    | 4001 |
| managers   | 5001 |

| LOGIN    | GECOS COMMENT   | SHELL         | UID#    | GROUPS             | PASSWORD | HOME              |
| :------- | :-------------- | :------------ | :-----: | :----------------- | :------- | :---------------- |
| database | DATABASE        | /sbin/nologin | 200     | database, dbadmin  |          | /var/lib/database |
| bob      | Robert Smith    | /bin/bash     | 2001    | managers           | Passw0rd | /home/bob         |
| joe      | Joe Evans       | /bin/bash     | 2002    | dbadmin,wheel      | Passw0rd | /home/joe         |

1. Type these commands in the terminal: 
2. `groupadd --gid 200 database  `
3. `useradd --comment DATABASE --gid database  --home-dir /var/lib/database database `
4. `groupadd --gid 4001 dbadmin `
5. `usermod --groups dbadmin database `
6. `id database `
- > Note that the UID took the next available number.
7. `getent passwd database `
- > Note that the SHELL is the default */bin/bash* and not */sbin/nologin*.
8. `usermod --shell /sbin/nologin  database `
9. `getent passwd database `
- > Confirm the SHELL is correct.
10. `usermod --uid 200 database `
11. `id database `
- > Confirm the UID, GID, and GROUPS are all correct.
- > NOTE: Of course all these values could have been set with one `useradd` command and the correct options. The purpose here is to practice **verifying and correcting** as needed.

![image](https://user-images.githubusercontent.com/36435980/145691745-bb6f33d9-f1ce-4755-9579-3453b60d2692.png)

12. `groupadd --gid 5001 managers `
13. `useradd --uid 2001 --groups managers --comment "Robert Smith"  bob  `
14. `echo Passw0rd | passwd --stdin bob `
15. `id bob `

![image](https://user-images.githubusercontent.com/36435980/145691901-7fce4cd1-cb9b-496e-9e71-b98a220d41a9.png)

16. `useradd --uid 2002 --groups dbadmin,wheel --comment "Joe Evans"  joe  `
17. `passwd joe  `
- > Enter **Passw0rd** when prompted.
18.  `id joe `

![image](https://user-images.githubusercontent.com/36435980/145691957-07f8e420-8ba6-4ea7-90d7-5529445608dd.png)

19. `grep -e 'database' -e 'joe' -e 'bob'  /etc/passwd  /etc/group  /etc/shadow  `
- > Refer to `man 5 passwd` or `man 5 group` or `man 5 shadow` for more information about these configuration files.
- > The `grep` command is covered in Chapter 4 of the ***Pearson RHCSA 8 Cert Guide***.

![image](https://user-images.githubusercontent.com/36435980/145692098-fb630577-8336-4384-8876-c4147ca30e38.png)

20. `exit `
21. `exit `
- > Log out of **SERVER1** completely.

******
# MANAGING USERS
## Administrative Privileges and Switching Users

### TRY IT - Using `su`

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `su --help | head -n 15  `
- > Review the syntax and options for the `su` command.

![image](https://user-images.githubusercontent.com/36435980/145692673-e2897a5c-e1e0-4dcd-8f36-898a12dad771.png)

3. `whoami `
4. `su --login `
- > Or use the equivalent `su -l` or `su - `. There are always many ways to get the desired results in the CLI shell.
- > Enter **Passw0rd!** when prompted.
5. `whoami ; pwd `
6.  `su -c "whoami ; pwd" user1  `
- > If the **user1** account was not created in the previous lab OR the Workstation VM was reset to an earlier snapshot where **user1** does not exist, recreate the account.
- > Note that the `su` command does not prompt the **root** user for passwords! 
7. `su -lc "whoami ; pwd"  user1 `
- > Note the difference between the PWD when using a non-login shell ( */root/* ) and a login shell ( */home/user1/* ).  
8. `exit `

![image](https://user-images.githubusercontent.com/36435980/145692898-fb0ac31e-b019-49a0-a0a0-e12664f64d53.png)

9. `id user2 `
- > Confirm **user2** exists.  Create the account and set or change the password to **Passw0rd** as needed.
10. `su -  user2 `
11. `id ; pwd ; echo $PATH `
- > Note the environment with a *login shell*.
12. ` exit `
13. `su user2 `
14. `id ; pwd ; echo $PATH `
- > Note the difference in the environment with a *non-login shell*.
15. `exit `

![image](https://user-images.githubusercontent.com/36435980/145693534-e6a3337b-650d-430b-8ece-c4034e915e88.png)

******
# MANAGING USERS
## Administrative Privileges and Switching Users

### TRY IT - Using `sudo`

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `man -k sudo`
- > Note the manuals for the */etc/sudoers* file and the `visudo` command.
3. `sudo --help | less`
- > Note the **`-i`**, **`-l`**, and **`-b`** options.
4. `sudo -l`

![image](https://user-images.githubusercontent.com/36435980/163049931-446e1df9-a09d-43b4-b777-006adff13547.png)

5. `whoami`
6. `sudo whoami`
7. `id`
8. `sudo id`
9. `sudo useradd fred`
10. `sudo --user=fred whoami`
11. `sudo --user=fred id`
- > The UID and GID numbers for **fred** may be different on your system.
12. `sudo userdel -r fred`

![image](https://user-images.githubusercontent.com/36435980/163051000-b8c54744-41dd-4300-870f-db2b62e9c458.png)

******

# ADMINISTRIATIVE PRIVILEGES AND SWITCHING USERS
## Lesson Review

### HANDS ON EXERCISE - Elevating Privileges and Switching Users

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `id bob`
- > Confirm the user **bob** from an earlier lab exists. Create the account and set the password to **Passw0rd** as needed.
5. `sudo -i `
6. `man visudo `
- > Read to the end of the second paragraph of the **DESCRIPTION** section of the manual.

![image](https://user-images.githubusercontent.com/36435980/145694622-8bb430be-c82f-4cd0-a0ed-5776db9fa816.png)

7. `man sudoers `
- Press **`</>`** slash to open a SEARCH prompt.
- Type `sudoers.d`**`<ENTER>`** and read the manual down to the paragraph explaining which characters in a file name under */etc/sudoers.d/* would exclude the file from being processed by the **#includedir** directive.

![image](https://user-images.githubusercontent.com/36435980/145694583-1488d006-e3e8-43ec-bccb-1b1357487e6e.png)

*****
### TASK 3: Configure `sudo` 
1. Configure `sudo` to allow user **bob** full admin privileges without a password. Type these commands in the terminal: 
2. `grep 'NOPASSWD' /etc/sudoers  `
- > Use this example to begin.
3. `grep 'NOPASSWD' /etc/sudoers  > /etc/sudoers.d/bob `
4. Make the file */etc/sudoers.d/bob* contain the following text:

```
bob  ALL=(ALL)    NOPASSWD:  ALL
```
- > Use I/O redirection or `vim /etc/sudoers.d/bob` as preferred
- > Adding this line at the bottom of the file */etc/sudoers* with the command `visudo` would have the same effect.
5. Log in to the **bob** account and confirm the `sudo` command works without a password.
    1. `su - bob `
    2. `whoami `
    3. `sudo whoami `
    4. `exit `
  
![image](https://user-images.githubusercontent.com/36435980/145694901-d9d4c0a3-4779-4a28-a116-0cdf52adafee.png)


*****

# PASSWORD AGING POLICIES
## Policy Settings and Configuration Files

### TRY IT - Viewing Password Policy Settings

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `man chage  `
3. Read the manual and find answers to the following questions:
    1. What 6 parameters can be set with the **OPTIONS** for `chage`?
    2. When using the `-E` or `--expiredate` option, what argument will remove an account expiration date?
    3. According the the **OPTIONS** section of the manual, what happens when `chage LOGIN ` is run with no options selected?
    4. According to the **NOTE** section, which option for `chage` is **not restricted to root** for unprivileged users to determine their password or account expiration dates?
    5. Which 3 configuration files are mentioned under the **CONFIGURATION** and **FILES** sections of the manual?

4. `man 5 shadow `
5. Read the manual and find answers to the following question:
    1.  Which character in the second field indicates a locked password?
    2.  What does a `0` in the third field mean?
    3.  What does it mean if the seventh field is empty?
  
6. `chage -l student `
7. `chage -l user2 `
- > Note that admin privileges are required to see information about users other than yourself.
8. `sudo !chage `

![image](https://user-images.githubusercontent.com/36435980/145695570-5bc7c487-17c1-4a9c-bce9-fd7d8112897e.png)


*****

# PASSWORD AGING POLICIES
## Configuring Password Policy Settings

### TRY IT - Configuring Password Policy Settings

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `sudo grep 'user2' /etc/shadow `
3. `sudo chage user2   `
- Change only the following values:
    1. Maximum Password Age: 90
    2. Password Expiration Warning: 10
    3. Password Inactive: 14
4. `sudo grep 'user2' /etc/shadow `
- > Which fields changed?

![image](https://user-images.githubusercontent.com/36435980/145695697-3ffea619-47e9-459c-993e-9953e2f591e4.png)

5. `sudo chage -l user2 `
6. `sudo chage --lastday 0  user2 `
7. `sudo chage -l  user2 `

![image](https://user-images.githubusercontent.com/36435980/145695746-a49bcf99-b8e2-45b4-b5fa-7d022e371280.png)

8. `ssh user2@localhost `
- > Note that **user2** must enter the current password before entering the new password!
- > Set the password to a more secure password of your choice (**PassTheEX200!!** for example).
- > The user will be logged out and must reconnect after changing their password.
9. `ssh user2@localhost `
- > Enter the NEW password when prompted.

![image](https://user-images.githubusercontent.com/36435980/145695902-20e68c70-0fa4-4328-a52a-684f6f5d2fbf.png)

******

# PASSWORD AGING POLICIES
## Lesson Review

### HANDS ON EXERCISE - Managing Users, Groups, Passwords, and Privileges

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `sudo -i `
5. `ls -lh /home `
- > Confirm the users **bob** and **joe** created in an earlier lab exist.  Recreate the accounts if needed.
6. `chage -l bob `

![image](https://user-images.githubusercontent.com/36435980/145896226-e1b38bed-283d-45a8-9c5d-08e4483e0c91.png)

7. Modify the policy settings for **bob** to the following:

| MIN PASS AGE | MAX PASS AGE | LAST PASS CHANGE | PASS EXPIRE WARNING | PASS INACTIVE | ACCOUNT EXPIRE DATE |
| :----------- | :----------- | :--------------- | :------------------ | :------------ | :------------------ |
| 3 DAYS       | 90 DAYS      | DO NOT CHANGE    | 10 DAYS             | 14 DAYS       | DO NOT CHANGE       |

8. `chage bob `
- > Follow the interactive prompts then confirm the correct settings were applied with `chage -l bob `

![image](https://user-images.githubusercontent.com/36435980/145897451-5170f874-54d1-4189-bde6-828394ef82e9.png)

9. `cp -v /etc/login.defs  ~/login.defs.bak `
- > Backup important config files before making changes!
- > Refer to `man login.defs` for more information as needed.
10. `vim  /etc/login.defs `

![image](https://user-images.githubusercontent.com/36435980/145897782-fd9f5b87-da50-4f59-8b7b-b83105f558ee.png)

11. Modify these lines in */etc/login.defs* as shown. 
```
PASS_MAX_DAYS        90
PASS_MIN_DAYS        3
PASS_MIN_LEN         5
PASS_WARN_AGE        10
```

![image](https://user-images.githubusercontent.com/36435980/145898458-a225b44b-7dbd-4352-a299-445798382a3d.png)

12. `chage -l joe `
- > Note that changing the defaults for new account creation in */etc/login.defs* will not change existing accounts!
13. `useradd -c "Bill Jones" bill `
14. `echo Passw0rd | passwd --stdin bill `
15. `chage -l bill `
- > Note that **bill** has the new password aging policy defaults from */etc/login.defs*.

![image](https://user-images.githubusercontent.com/36435980/145899240-6db748dd-649c-4924-a995-5c90e90f5367.png)

16. `exit `
17. `exit `
- > Log out of **SERVER1** completely.

******

# MANAGING USERS (pages 135-138)
## Module Review

### END OF MODULE LAB - Managing Users

> Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the ***~student*** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### TASK 3:  Perform the following operations on SERVER2
1. `sudo -i `
2. `cp -v /etc/login.defs ~/ `

3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 135 
4. Complete **Exercise 6-2** from the book
- > Note that `passwd ` also has options to manage password aging policy similar to `chage `.
5. Open the ***Pearson RHCSA 8 Cert Guide*** to page 138 
6. Complete **Exercise 6-3** from the book

### SOLUTION

![image](https://user-images.githubusercontent.com/36435980/146276026-3d6c236a-0ac9-45f3-a52f-4912f4345aad.png)

![image](https://user-images.githubusercontent.com/36435980/146276251-792f1a17-417b-46fc-b40a-750c53e725d8.png)

![image](https://user-images.githubusercontent.com/36435980/146276695-1d4db36f-c042-4245-ac92-2e000dc5dc31.png)

![image](https://user-images.githubusercontent.com/36435980/146277072-437bcb54-97cc-41a1-96ba-af1bfdc1d3e9.png)

*****

![image](https://user-images.githubusercontent.com/36435980/146277636-6f8d412a-fde4-4156-be33-69c4827c6a1f.png)


******
