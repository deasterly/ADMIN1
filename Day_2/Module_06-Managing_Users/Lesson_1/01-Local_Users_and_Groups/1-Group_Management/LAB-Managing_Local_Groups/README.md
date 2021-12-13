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
*****
*****
