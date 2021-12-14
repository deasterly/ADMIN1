# PERMISSIONS BASICS (pages xx-yy)
## Lesson Review

### HANDS ON EXERCISE - Basic Permissions Practice

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
2. `ssh student@192.168.4.3 `
- > Enter **Passw0rd** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `sudo -i `
5. `ls -lh /home `
- > Confirm the users **bob** and **joe** created in an earlier lab exist.  Recreate the accounts if needed.
6. `id bob ; id joe `
- > Confirm **bob** is a member of the group **managers** and **joe** is a member of the group **wheel**.
- > Recreate groups and modify users as needed.
7. `su -l  joe `

![image](https://user-images.githubusercontent.com/36435980/146076307-ef755058-cb47-48cb-8693-c470a8419289.png)

8. `sudo mkdir -v /home/reports `
9. `ls -ld /home/reports `
10. `sudo chown -v joe:managers /home/reports ` 
11. `sudo chown -v  u=rwx,g=rx,o-rwx  /home/reports  `
- > This combination of ownership and permissions allows **joe** full control over */home/reports/* while allowing **bob** or any other member of **managers** have read-only access to the contents.

![image](https://user-images.githubusercontent.com/36435980/146077332-1bcc61e8-d8d6-46d6-b4cf-38c36ca562e7.png)

12. `cd /home/reports `
13. `df -h > filesystems_report.txt `
14. `lsblk > disk_report.txt `
15. `ls -lh `
16. `exit `
17. `su -l bob `
18. `cd /home/reports `
19. `mkdir -v managers `
- > Notice the error message.  The group **managers** does not have the **write** permission.
20. `cat filesystem_report.txt `
21. `rm --force  disk_report.txt `
- > The **write** permission on the parent directory is required to delete a file.
22. `exit `
23. `exit `
24. `exit `
- > Log out of **SERVER1** completely.

![image](https://user-images.githubusercontent.com/36435980/146079499-4a051b5a-cf38-4336-807c-ec5e1f009dc9.png)

******

******

******

