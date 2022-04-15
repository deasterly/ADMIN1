# PROCESS BASICS (pages 233-251)
## MANAGING PROCESSES

### TRY IT - Job Control

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Use BASH shell job control

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Type these commands in the terminal: 
2. `sudo -i `
- > Confirm you are now user **root** on **Workstation**
3. Review documentation from these commands:
    1) `help jobs`
    2) `help bg`
    3) `help fg`
3. Open the ***Pearons RHCSA Cert Guide*** to page 238
4. Complete **Exercise 10-1** from the book

******

# SIGNALS (pages 239-242, 244-248)
## SENDING SIGNALS TO PROCESSES

### TRY IT - Sending Signals to Processes

> ### Perform the following tasks on the **Workstation VM** as user **student**.
> In this lab you will perform the following tasks:
- Send signals to processes

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~student** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Read pages 244-245 of the ***Pearson RHCSA Cert Guide***
2. Type these commands in the terminal: 
    1) `sleep 10000 `
    2) Press **`<CTRL+c>`** to interrupt the process
    3) `sleep 10000 &`
    - > Run this command 2 more times to have 3 jobs running in the background
    4) `jobs`
    5) `fg 1`
    - > Bring the first `sleep` job to the foreground
    6) Press **`<CTRL+z>`** to stop the foreground job
    7) `bg 1`
    - > Return the stopped job to running in the background
    8) `jobs`
    9) `pgrep sleep`
    - > Take note of the PIDs listed referenced as (PID1)-(PID3) in upcoming commands
    10) `kill -l`
    - > Notice the different signals that can be sent to processes by `kill`
    11) `kill -9 (PID3)`
    12) `kill -SIGINT (PID2)`
    - > Pay attention to the difference in the output of the last 2 commands
    13) `killall -TERM sleep`
    14) `jobs`

******

# PROCESS BASICS
## MODULE 8 REVIEW

### END OF MODULE LAB - Process Basics

> ### Perform the following tasks on the **Server2 VM** as user **root**.
> In this lab you will perform the following tasks:
- Manage jobs and processes

******
### STEP 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Confirm you are logged in to the correct host and starting from the the **~root** home directory.
3. Log out and connect using the correct host and/or user as needed.
******
### STEP 2: Perform the following operations
1. Open the ***Pearson RHCSA Cert Guide*** to page 245
2. Complete **Exercise 10-2** from the book

******
