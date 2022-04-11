# MANAGING USERS
## Administrative Privileges and Switching Users

### TRY IT - Using `sudo`

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
2. `mandb  `
3. `yum -y install man-pages `
4. `useradd testuser `
- > The errors occur because commands run as **student** do not execute with admin privileges.
5. `sudo mandb `
- > Enter **Passw0rd** if prompted.  The search cache should update successfully. 

![image](https://user-images.githubusercontent.com/36435980/145693811-a0c39b01-0110-4f3f-b288-f57c2bf13c34.png)

6. `sudo !yum `
- > This *history expansion* will repeat the previous `yum` command with admin privileges.
- > Note that `sudo` will temporarily cache your credentials after authenticating successfully.
7. `man -k sudo `

![image](https://user-images.githubusercontent.com/36435980/145693886-5066f7d3-8ee2-4461-ba5d-49d63a97b6c5.png)

8. `man sudo `
- Press the **`</>`** slash key to open a SEARCH prompt.
- Type `^EXAMPLES<ENTER>` in the prompt, read the EXAMPLES section of the manual, then quit with **`<q>`**.

![image](https://user-images.githubusercontent.com/36435980/145694012-0c9c1139-0c20-4ded-9ca0-81d78f310a3e.png)

*****

*****

*****
