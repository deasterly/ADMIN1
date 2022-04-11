# MANUALS
## Searching Manuals

### TRY IT - Searching the Manual Database

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Search manual pages
1. Type these commands in the terminal: 
2. `sudo mandb `
- > Enter ***Passw0rd*** when prompted.
3. `man -k manual `
- > Note that `man -k STRING ` searches for STRING in the **TITLE** and **NAME** sections of the manual pages.
4. `man -f passwd `
- > Note that `man -f STRING ` searches for STRING only in the **TITLE** section of the manual pages.
5. `whatis passwd `
- > Note that `whatis` and `man -f` are synonymous.

![image](https://user-images.githubusercontent.com/36435980/144491599-cdf94885-c5ae-459b-a45a-526294322d4f.png)

6. `man -k regex `
7. `apropos regex `
- > Note that `apropos` and `man -k` are synonymous.

![image](https://user-images.githubusercontent.com/36435980/144491510-7e180740-8162-4c84-b052-bfcf9ddf9216.png)

8. `man -K dell.com `
- > Use `less` searching - remember **`<h>`** for help - to find the matching text in the open manual.

![image](https://user-images.githubusercontent.com/36435980/144491459-93c48d85-911e-4d52-b466-4939789485c1.png)

9. `man -K dell `
- > Find the matching text in two or more manuals. 

![image](https://user-images.githubusercontent.com/36435980/144491312-ffaf9c42-37a9-4060-81f2-50f8a58e413a.png)

- > Skip results with **`<CTRL+d>`** and quit with **`<CTRL+c>`** after you have mastered searching manuals.

******
