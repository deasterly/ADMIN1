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
| database | DATABASE        | /sbin/nologin | 200     | database, dbadmins |          | /var/lib/database |
| bob      | Robert Smith    | /bin/bash     | 2001    | managers           | Passw0rd | /home/bob         |
| joe      | Joe Evans       | /bin/bash     | 2002    | dbadmins,wheel     | Passw0rd | /home/joe         |

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

******

******
