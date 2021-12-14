# PERMISSIONS BASICS
## Setting Ownership and Permissions

### TRY IT - Setting File Ownership and Permissions

> Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `pinfo chown  `
- > Read down to the paragraph ending with `*Note Disambiguating names and IDs::`
3. `pinfo coreutils --node="File permissions" `
- > Refer to this documentation for more information about *Symbolic Modes* and *Numeric Modes* as needed.
4. `chmod --help `
- > Note that multiple *Symbolic Modes* can be separated by commas.
- > The **OCTAL-MODE** is explained in the *coreutils.info* under *Numeric Modes*. 
5. `cp /usr/share/dict/words ~/ `
6. `ls -l words `
7. `id `
- > Confirm you are a member of the group **wheel**.
8. `chown -v  :wheel words `
- > Note that the owner of a file or directory can only change the group ownership if they are members of that group.
9. `chown -v  root:root words `
- > Note the error message.  Administrative privileges are required to change the owner to any other user or the group owner to any group of which you are not a member.
10. `chmod -v a=rw words `
- This give everyone **read** and **write** on the file.  Note the OCTAL permission numbers.
11. `chmod -v o-rw words `
- > This removes **read** and **write** from **other**.  Note the OCTAL permission numbers.
12. `chmod -v g=r  words `
- > This gives the owning group **read** only.  Note the OCTAL permission numbers. 

![image](https://user-images.githubusercontent.com/36435980/146073942-8e85def7-c00a-4c5c-a84b-65d3a5f74701.png)

*****

*****

*****

