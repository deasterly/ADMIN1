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

******

******
