# ARCHIVING
## Using the `tar` Tape Archiver

### TRY IT - Tar Archiving

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
2. `tar --help | less `
- > Review the *EXAMPLES* and *Compression Options* in the help then exit `less` when done.
3. `mkdir -v /tmp/backup  /tmp/restore `
4. `sudo tar  -cf  /tmp/backup/backup.tar   /etc    /var/log    /root `
- > Note that `tar` removes leading forward slashes from file paths to make the archive contents a *relative path* rather than the *absolute path* that was used in the command.
5. `sudo  tar  -caf  /tmp/backup/backup.tar.xz    /etc   /var/log    /root `
6. `ls  -ahl  /tmp/backup/ `
- Compare the sizes of the compressed and uncompressed archives.

![image](https://user-images.githubusercontent.com/36435980/145628348-379ecb04-47b3-4ef5-935c-b6bb8ff13b69.png)

7. `cd  /tmp/restore `
8. `file  /tmp/backup/* `
9. `sudo  tar  -tvf  /tmp/backup/backup.tar.xz | less `
- > Note that the `tar` archive preserves important information like ownership, permissions, and timestamps.
10. `sudo  tar  -xf  /tmp/backup/backup.tar.xz  `
11. `ls  -lh `

![image](https://user-images.githubusercontent.com/36435980/145628567-a8ba1086-c27e-41cf-962d-6078d6479392.png)

*****
