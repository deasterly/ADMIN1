# CONTROLLING `systemd` (pages 252-268)
## MANAGING SERVICE UNITS

### TRY IT - Controlling Services Using `systemctl`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use `systemctl` to manage service units

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `systemctl list-units --type=service`
3. `systemctl status sshd`
4. `sudo systemctl disable sshd`
5. `systemctl status sshd`
6. `sudo systemctl enable sshd`
7. `systemctl status sshd`
8. `sudo systemctl stop sshd`
9. `systemctl status sshd`
10. `sudo systemctl start sshd`
11. `systemctl status sshd`


******

# CONTROLLING `systemd` (pages 252-268)
## MANAGING TARGET UNITS

### TRY IT - Controlling Targets Using `systemctl`

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use `systemctl` to manage target units


******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `systemctl get-default`
3. `sudo systemctl set-default multi-user.target`
4. `sudo systemctl isolate multi-user.target`
5. `sudo systemctl isolate graphical.target`
6. `sudo systemctl reboot`
- > From the Workstation VM Console log in as **student** again
7. `sudo systemctl set-default graphical.target`
8. `sudo systemctl reboot`

******

# CONTROLLING SYSTEMD
## MODULE REVIEW

### END OF MODULE LAB - Controlling `systemd`

> ### Perform the following tasks on the **Server2 VM** as user **root**.
> In this lab you will perform the following tasks:
- Use `systemctl` to manage units

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~root** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Open the ***Pearson RHCSA 8 Cert Guide*** to page 261
2. Complete **Exercise 11-1** from the book

******
