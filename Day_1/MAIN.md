<PRE>
Module_00-Class_Introduction/
├── 01-Course_Introduction
├── 02-Lab_Info
├── 03-Agenda_and_Objectives
└── 04-Additional_Linux_Study_Resources
</PRE>

# RHCSA v8.2 Certification Prep
## Admin 1

### Pearson RHCSA 8 Cert Guide

*****
## What will you learn?
- How to use, configure, and administer RHEL8-compatible Linux distributions
- Objectives for the Red Hat RHCSA8 certification exam (EX200)

## What will you need?
- Do you have:
  - Prior Linux experience?
    - If not, please take **"Intro to Linux"** first
  - Your book?
    -  *Red Hat RHCSA 8 Cert Guide by Sander van Vugt*
  -  Your lab information?
  -  A way to take **good notes?**

*****
## Lab Environment Information

- VLP Lab Environment information provided by instructors 

### Self-Study Options
- *"Linux in a Box"* project in MS Teams
- Red Hat Developer Subscription to build your own RHEL8 projects and labs
  - https://developers.redhat.com/register to get started
  - Free subscription to updates, Red Hat KB, and more
 
 *****

| **Day 1** | **Day 2** | **Day 3** | **Day 4** | **Day 5** |
| :---- | :---- | :---- | :---- | :---- |
| *Using the CLI* | *Configuring BASH* | *Controlling **systemd** Units* | *Software Packages* | *Managing Servers* |
| - Using the BASH Shell CLI | - Variables | - Service units | - Module Streams | - NTP |
| - Running commands | - Config files | - Target units | - Adding repos | - Basic webservers |
||||||
| *Documentation* | *Managing Users* | *Configuring SSH* | *Networking* | *Deploy a Server Lab* |
| - Built-in Help | - Users & Groups | - SSH features | - CLI commands | - Installation |
| - Manuals | - Admin privileges | - Key-based auth | - Config files | - Configuration |
| - GNU Info | - Password polices | - Securing SSH | - Troubleshooting | - Testing |
||||||
| *Working with Text* | *File Permissions* | *Configuring Logging* | *Basic Storage* ||
| - The **VIM** Editor | - UGO/RWX basics | - Syslog logging | - Partitions ||
| - I/O Redirection | - Special Permissions | - Journal logging | - File systems ||
||||||
| *Working with Files* | *Process Basics* | *Software Packages* | *Cockpit* ||
| - GNU Coreutils | - Job control | - Find & install software | - Web console ||
| - Archiving | - Signals | - Package queries | - Diagnostic reports ||
||||||

******

## RHCSA Certification Info and Resources

- Study and learn all the RHCSA EX200 Exam Objectives
  - https://tinyurl.com/rhcsaexaminfo 
- Get your course reference book by Sander van Vugt
  - https://pearsonitcertification.com
- Find on-demand resources in the Dell Learning Studio
  - Join the “Linux Certification Help” group at https://learningstudio.dell.com/teams/linux-certification-help 
- Find tips for passing Red Hat exams, info about exam testing at home, cheat sheets, and more from the Linux Training Delivery site
  - https://dell.sharepoint.com/sites/LinuxTrainingDelivery 

*****

<PRE>
Module_01-Using_the_BASH_CLI_Shell/
├── Lesson_1
│   ├── 01-Bash_Shell_Features
│   │   └── LAB-Working_Efficiently_in_the_Shell
│   ├── 02-BASH_History
│   │   └── LAB-Using_BASH_History
│   ├── 03-BASH_Special_Metacharacters
│   │   └── LAB-Using_BASH_Metacharacters_Correctly
│   ├── 04-BASH_Completion_and_Expansion
│   │   └── LAB-Using_BASH_Shell_Expansions
│   └── 05-Lesson_Review
│       └── LAB-BASH_Shell_Essentials
├── Lesson_2
│   ├── 06-Types_of_Commands
│   │   ├── 1-Shell_Built-ins
│   │   │   └── LAB-BASH_Builtins
│   │   ├── 2-External_Commands
│   │   │   └── LAB-External_Commands
│   │   └── 3-Aliases
│   │       └── LAB-BASH_Aliases
│   └── 07-Lesson_Review
│       └── LAB-Using_Commands_and_Aliases
└── Module_Review
    └── LAB-Using_the_CLI
</PRE>


# EX200 PREP

# Lesson 1 - Using the BASH Shell

## BASH Shell Features
- Run `pinfo bash --node="Basic Shell Features"  ` 

![image](https://user-images.githubusercontent.com/36435980/143947858-55ede74f-cf96-40e2-a1ff-a02191e32829.png)

*****
## BASH Shell Features
- USE: Keyboard shortcuts to save time and typing in BASH

![image](https://user-images.githubusercontent.com/36435980/143949892-1f4ed6cd-e966-4fc0-99fa-83ac73cd1538.png)

- USE: **`<TAB>`** completion for commands, file paths, and options/switches
- Run `pinfo bash --node="Command Line Editing"  `

![image](https://user-images.githubusercontent.com/36435980/143949684-d8697a2a-7df8-4138-9046-0fd68746360d.png)

*****

# BASH Shell Basics 
## BASH Shell Features

### TRY IT - Working Efficiently in the Shell

> ### Perform the following tasks on the Workstation VM Console as user **student**.

******
### TASK 1: Log in to Workstation as user **student**
1. Log in to the Ubuntu Desktop as user **student** using **Passw0rd** for the password
![image](https://user-images.githubusercontent.com/36435980/143912652-69dda936-dea6-4e25-b755-0e0726291d78.png)

2. On the Ubuntu Desktop open Virtual Machine Manager 
![image](https://user-images.githubusercontent.com/36435980/143913153-b96fdd6d-4b46-4cae-b534-43be27eaabd9.png)

3. Launch the Workstation VM console
- > Unlock the screen if required

![image](https://user-images.githubusercontent.com/36435980/143913276-a0d1af48-d552-4bb2-9108-26de56493889.png)

4. Log in as **student** using **Passw0rd** for the password
![image](https://user-images.githubusercontent.com/36435980/143913326-b2e22bb0-8128-433b-a827-8498ac6eb620.png)

5. Open a Terminal
![image](https://user-images.githubusercontent.com/36435980/143913351-9bea6cd4-8fac-45af-83f2-295c7e145425.png)

******
### TASK 2: Type the following in the terminal: 
1. `ls <ENTER>`
2. `pwd <ENTER>`
3. `ls ; echo ; pwd <ENTER>`
- > Note that commands separated by **`;`** run sequentially.

![image](https://user-images.githubusercontent.com/36435980/143913599-c5b83c9d-49e4-48c8-bedc-14725867c600.png)

4. `ls --<TAB x2>` 
- > Notice that when there are multiple auto-complete options available, you must use **`<TAB>`** twice.

![image](https://user-images.githubusercontent.com/36435980/143913734-1527224e-af50-4eef-a1ce-c2040e331f1e.png)

5. `ls --v<TAB><ENTER>`  
- > Notice the option auto-completed with a single **`<TAB>`**.         
6. `ls --r<TAB x3>` 
- > Notice the letter **`e`** auto-completes after the first **`<TAB>`** then the full options appear after pressing **`<TAB>`** twice more.
  Choose to list the contents in reverse order by typing **`v<TAB><ENTER>`** or recursively by typing **`c<TAB><ENTER>`**.

![image](https://user-images.githubusercontent.com/36435980/143914307-90de27c2-5df8-4882-9094-58c18c261f8d.png)

7. `ls -ld  ~/D<TAB x2>`
- > Choose to list the *~/Desktop/* directory by typing **`e<TAB><ENTER>`** or continue choosing between *~/Documents/* and *~/Downloads/* by typing **`o<TAB x2>`** then typing either   **`c<TAB><ENTER>`** or **`w<TAB><ENTER>`**.

![image](https://user-images.githubusercontent.com/36435980/143914402-b97a0ba3-4008-4fd1-a065-2b196fba05de.png)

8. `ls<TAB x2>`
- > Notice many more commands start with `ls`.
9. `lsc<TAB><ENTER>`
- > View CPU information.
10. `lsb<TAB><ENTER>`
- > View storage block device information.
  Notice that auto-completion only requires a single **`<TAB>`** when there a no more ambiguous matches.
11. `<CTRL>+l`
- > Notice this clears the terminal like the command `clear`.
12. `<CTRL>+d`
- > Notice this logs the user out of their shell.

![image](https://user-images.githubusercontent.com/36435980/143914513-4fceef89-4542-442e-a31f-81a53723a4f4.png)

******

## BASH History
- Understand: History is *built-in* to the shell
- Understand: Personal history is stored in the *~/.bash_history* $HISTFILE
- Use: Multiple ways to perform history expansion
- Run `pinfo bash --node="Using History Interactively"  `

![image](https://user-images.githubusercontent.com/36435980/143948203-6e5118c2-8d28-42c9-b22d-17678f0fa1ec.png)

*****

# USING THE BASH CLI SHELL
## BASH History

### TRY IT - Using BASH History

> ### Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `help history `
- > Take a moment to read the help and take note of the HISTFILE location.	

![image](https://user-images.githubusercontent.com/36435980/144289557-802fc6d0-f714-4ac5-b721-92cd6fe7f537.png)

3. `history ` 
- > Use the up arrow to scroll through previous commands and notice they match the history output.

4. `!echo `
- > Notice this reprints the most recent line in the history starting with 'echo' and repeats the command.

5. `echo $(whoami) `
6. `!!<ENTER> `
- > Notice that typing '!!' will repeat the most recent command from the history.

7. `echo !1<ENTER> `
- > Notice this repeats the earliest command from your history.

8. `env | grep 'HIST' `
- > Notice that the maximum  size of the history and that duplicate commands are not repeated in the history.

9. `^HIST^HOST^<ENTER> `
- > Notice that you can perform history substitutions using the **'^'** character.

![image](https://user-images.githubusercontent.com/36435980/144289671-07f645b4-f9eb-45a0-9313-0bb4b2293892.png)

*****

## BASH Special Metacharacters
- Run `pinfo bash --node="Definitions" ` 
  - See ”Control Operators” and "Metacharacters" 

![image](https://user-images.githubusercontent.com/36435980/143950523-b03ce3a1-9f6d-420b-abc2-813e33db61d9.png)

![image](https://user-images.githubusercontent.com/36435980/143950552-bb2e2ffc-cc7a-44d8-8728-2099058e1a2d.png)

- Use: Quoting, escaping, control operators, parameter/variable expansion, and some useful simple pipelines 

![image](https://user-images.githubusercontent.com/36435980/143950746-3386b187-a10a-4f76-8da8-ef35e3682ce1.png)

![image](https://user-images.githubusercontent.com/36435980/143950808-074724b5-09b6-4e48-9916-180e909b4ec3.png)

*****

# USING THE BASH CLI SHELL
## BASH Special Metacharacters

### TRY IT - Using BASH Metacharacters Correctly

> ### Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `echo  $SHELL and  "$HOME" compared to  ;  echo   \$SHELL vs. '$HOME'  `

![image](https://user-images.githubusercontent.com/36435980/144291792-fcc2b43d-4311-497d-94de-062ffbb9fbcf.png)

- > Review the BASH info documentation for quoting and escaping by running `pinfo bash --node="Quoting" `

![image](https://user-images.githubusercontent.com/36435980/144291008-539396f8-3713-433c-9225-0151c5a1979e.png)

3. `ls /usr/share/doc `
- > Notice there are multiple lines of output.
4. `ls /usr/share/doc | less `
- > Notice piping the output to `| less` displays one page of output at a time. 
- > Press **`<h>`** for help and **`<q>`** to quit.
5. `ls /usr/share/doc | wc -l ` 
- > Notice piping the output to `| wc -l` reports how many lines the command sends to STDOUT.
6. `ls /usr/share/doc | grep cat `
- > Notice piping the output to `| grep <STRING> ` only displays matches for the search string.
	
![image](https://user-images.githubusercontent.com/36435980/144291910-be9c4525-2553-4ce8-8816-0efec557b972.png)

******
*****

## BASH Completion and Expansion
- Use: Tilde expansion, brace expansion, and command substitutions
- Run `pinfo bash --node="Shell Expansions"  `  

![image](https://user-images.githubusercontent.com/36435980/143951150-515e41b5-298e-453d-99aa-f9e5b4e253a2.png)

![image](https://user-images.githubusercontent.com/36435980/143951240-fcdaf6a1-69a4-47aa-9bd2-4453f2f039bb.png)

*****

# USING THE BASH CLI SHELL
## BASH Completion and Expansion

### TRY IT - Using BASH Shell Expansions

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Use Filename Expansion
1. Type these commands in the terminal: 
2. `man 7 glob `
- > Globbing is another name for **Filename Expansion**
- > Read the DESCRIPTION to the end of the "Ranges" section then press **`<q>`** to quit.

![image](https://user-images.githubusercontent.com/36435980/144292845-31523e9f-dea8-4073-8bca-d4c09323c4f5.png)

3. Practice using the following filename expansions (a.k.a. "globbing")
- `ls -ld D* `
- `ls -ld ?e* `
- `ls -ld ?o* `
- `ls -ld ?[oe]* `
- `ls -ld ?[^oe]* `
- `ls -ld ?[!oe]* `
	
![image](https://user-images.githubusercontent.com/36435980/144293392-7f128f3e-f4b1-4dff-9544-b4955d98f8e5.png)
	
### TASK 3: Use Command Substitution
1. Type these commands in the terminal: 
2. `man bash `
- > Type `/Command Substitution$<ENTER> ` then read to beginning of **"Arithmetic Expansion."**  Type **`<q>`** to quit when done.

![image](https://user-images.githubusercontent.com/36435980/144294073-08af8968-8680-44ca-818e-0c5a973c3ab0.png)

3. `echo  'whoami' versus `\` `whoami` \`
- > Notice that the second quotation marks are \` `backtick quotes` \` and not regular ` 'single quotes.' `

4. `echo "My working directory is $(pwd)." `
- > Notice there are two ways - \` `<commands>` \` and ` $(<commands>) ` -  to perform command substitutions.

![image](https://user-images.githubusercontent.com/36435980/144297134-c3bb8617-d2da-4263-8915-9457670fad8f.png)

### TASK 4: Use Tilde Expansion
1. Type these commands in the terminal: 
2. `man bash `
- > Type `/Tilde Expansion$<ENTER> ` then read the first paragraph.  Type **`<q>`** to quit when done.)

![image](https://user-images.githubusercontent.com/36435980/144297213-4c909eef-0150-4deb-ba60-96647aac8271.png)
	
3. `echo My user $USER has a home at ~ and root has a home at ~root `
- > Notice the tilde with no name expands to **$USER**'s home while **~NAME** expands to the home of **NAME**.
4. `echo "My user $USER has a home at ~ and root has a home at ~root " `
- > Notice that **tilde expansion does not work inside quotes**, even though variable/parameter expansion does.

	![image](https://user-images.githubusercontent.com/36435980/144297539-649d027d-9989-43cd-b631-cae1245c3e72.png)

### TASK 5: Use Brace Expansion
1. Type these commands in the terminal: 
2. `man bash `
- > Type `/Brace Expansion$<ENTER> ` then read the first 5 paragraphs.  Type **`<q>`** to quit when done.

![image](https://user-images.githubusercontent.com/36435980/144297830-2dd6bb5f-7c73-41c4-a36d-831fc164ed4a.png)

3. Practice using the following Brace Expansions
- `echo Example-{1..5} `
- `echo Example-{a,e,i,o,u} `
- `echo "Example-{1..5}" `
  - > Notice that **brace expansion does not work inside quotes**.

******

## Lesson Review

# USING THE BASH CLI SHELL (pages 38-39)
## Lesson Review

### HANDS-ON EXERCISE - BASH Shell Essentials

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Complete the following steps
1. Open the ***Pearson RHCSA 8 Cert Guide*** to page 38 
2. Complete **Exercise 2-3** from the book
3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 39
4. Complete **Exercise 2-4** from the book

******

# EX200 PREP

# Lesson 2 - Running Commands

![image](https://user-images.githubusercontent.com/36435980/143952146-000c113f-a867-4ff8-8c33-1737105037e3.png)

*****
## Types of Commands
- Understand: Shell Built-ins
- Run `man builtins` and  `help | less`

![image](https://user-images.githubusercontent.com/36435980/143952275-dfd1f093-c983-4874-8e1c-7badd40895e1.png)

*****
# TYPES OF COMMANDS
## Shell Builtins

### TRY IT - BASH Builtins Lab

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `help | less ` 
- > Take a moment to read the top paragraph and list of built-in commands.

![image](https://user-images.githubusercontent.com/36435980/144315840-25f782be-217e-4d7c-bcf4-eaf4a5bafe67.png)

3. `rpm -ql bash | less `
- > Pay attention to all the files in */usr/bin/* that correspond to the BASH builtin commands

![image](https://user-images.githubusercontent.com/36435980/144316149-6a84def7-8da1-456e-a32a-8c80487ddf25.png)
	
4. `which cd `
5. `cat $(which cd) `
6. Review the `help` for the following builtin commands
- `help for `
- `help export `
- `help umask `

![image](https://user-images.githubusercontent.com/36435980/144316453-11000e03-6ed4-4e94-ac34-8c545c03aa5b.png)


*****
## Types of Commands
- Understand: External commands
- Understand: Binary executables and interpreted scripts
- Run `file /usr/bin/ls ` and `file /usr/bin/gettext.sh ` 

![image](https://user-images.githubusercontent.com/36435980/143952479-7a88ee0a-b991-4de6-a69c-1672cc3e8bb1.png)

*****

# TYPES OF COMMANDS
## External Commands

### TRY IT - Exernal Commands

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `which cp `
3. `file $(which cp) `
- > Notice the output of `file` indicates this is a binary executable
4. `which zcat `
5. `file $(which zcat) `
- > Notice the output of `file` indicates this is a text executable script
6. `less $(which zcat) `

![image](https://user-images.githubusercontent.com/36435980/144317778-eb2b785f-569a-41df-b274-5b0dafe7e566.png)

******

## Types of Commands
- Understand: BASH Shell Aliases
- Run `help alias` and `which ls` 
  - Example: Compare the difference between ls -l /  and   \ls -l /

![image](https://user-images.githubusercontent.com/36435980/143952644-22747815-83a9-4e28-9bae-b450aa06e68e.png)

*****
# TYPES OF COMMANDS
## Aliases

### TRY IT - BASH Aliases

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Identify Aliases
1. Type these commands in the terminal: 
2. `which ll `
3. `alias -p `

![image](https://user-images.githubusercontent.com/36435980/144318636-7a8924c1-f99a-441b-98e5-a8fda0a62934.png)

4. `grep 'alias'  /etc/profile.d/*.sh `
- > Note that most aliases are defined by the BASH startup files. These will be covered in detail later.	

![image](https://user-images.githubusercontent.com/36435980/144318932-e1f28151-5b6b-4d8a-8b96-586afe6e8a57.png)

5. `sudo -i `
- > Enter ***Passw0rd*** when prompted.
6. `alias -p `
- > Notice that **root** has aliases for `mv` and `rm` that student does not have.
7. `exit `

![image](https://user-images.githubusercontent.com/36435980/144319179-4752c908-7dd1-4345-8983-c3b7aa95d785.png)

### TASK 3: Create Aliases 	
1. Type these commands in the terminal: 
2. `help alias `
- > Take a moment to read the help.
3. `labtest `
- > This will result in a **`"command not found"`** error, which is expected.
4. `alias labtest='echo Hello world' `
- > Note the use of single quotes and not backtick quotes after the `=` sign.
5. labtest

![image](https://user-images.githubusercontent.com/36435980/144319772-93f604f0-3bc9-4247-8b46-5ec5bab2fe29.png)

******

*****

# TYPES OF COMMANDS
## Lesson Review

### HANDS ON EXERCISE - Using Commands and Aliases

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter ***Passw0rd*** for the password when prompted.  
3. Type the following in the SSH terminal on server1
4. `ps<TAB>`
- > Notice nothing happens with a single **`<TAB>`**.
5. `ps<TAB x2> `
- > Notice the options available to us that start with the letters `ps`
6. `pst<TAB> `
- > BASH now has enough characters to autocomplete the command unambiguously.
7. `pstree ` 
8. `cd /etc`
9. `cat gro<TAB  x2> `
- > Note that the possible matches are still ambiguous.
10. `cat grou<TAB> `
- > A single **`<TAB>`** autocompletes when there are no other possible matches.
11. `cat group | wc -w `
- > Count the number of "words" (as understood by  `wc`)
	
### TASK 3: Use expansion with commands and aliases
1. Type the following in the SSH terminal on **server1**
2. `cd ~ ` 
3. `date --help | less `
- > Note the FORMAT string options for MM/DD/YY dates, HH:MM:SS times, weekday names, and others that may be useful.
4. `echo "Today is $(date +%A) $(date +%D) and the current time is $(date +%r)." `
5. `file $(which uptime) `
6. `file /usr/share/dict/linux.words `
7. `wc -l /usr/share/dict/linux.words `

![image](https://user-images.githubusercontent.com/36435980/144326265-d04352e0-9e2f-4210-99c3-18e85c837798.png)

8. `alias today='echo "Today is $(date +%A), $(date +%D) and the current time is $(date +%r)."  ' `
9. `which today `
10. `today `
11. `logout `

![image](https://user-images.githubusercontent.com/36435980/144326525-4b343fb5-99f4-4fd4-b5b5-ca608fa145da.png)
	
### TASK 4: Complete the following operations	
1. Return to the terminal on Workstation and type the following:
2. `alias -p `
3. `which labtest `
- > Note that this will only work as shown if the SSH connection to **server1** was made from the same shell where this alias was created.
4. `unalias labtest `
5. `which labtest `

![image](https://user-images.githubusercontent.com/36435980/144327077-b75e8b06-f312-4e84-bb2e-c23a557831d6.png)

6. `echo $SHELL `
7. `cat /etc/shells `
8. `sudo yum -y install zsh `

![image](https://user-images.githubusercontent.com/36435980/144327326-01591696-e2f1-46b4-ada0-75925490d90a.png)

10. `cat /etc/shells `
11. `exit `
	
![image](https://user-images.githubusercontent.com/36435980/144327378-9c98e3c4-7f0b-490a-9b2f-4c3d47ce1ac3.png)
	
******

## Module Review

![image](https://user-images.githubusercontent.com/36435980/143947048-75d4e7b0-3f09-40a8-aaa3-af967b1e1b62.png)


# USING THE BASH CLI SHELL
## MODULE REVIEW

### END OF MODULE LAB - Using the CLI

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******

### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.

******

### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

*****

### TASK 3:  Perform the following operations on SERVER2

1. Display only the first 10 lines of */usr/share/dict/words*
2. Display only the last 17 lines of */usr/share/dict/words*
3. Display the date in seconds since Jan 1st, 1970
4. Run the command that will show you the file type for */etc/group*
5. Run the command that will show you the absolute path to the command `uptime`
6. Determine what type of file is `uptime`
7. Show how many words are in the file */usr/share/dict/linux.words*
8. Create an alias called `utctime` that shows the time in UTC

*****

### SOLUTION

- > NOTE:  There may be many additional correct solutions other than those provided as examples in this guide.

1. Display only the first 10 lines of */usr/share/dict/words*

![image](https://user-images.githubusercontent.com/36435980/144328823-c5721147-f6a2-4294-8797-05db31502048.png)

2. Display only the last 17 lines of */usr/share/dict/words*

![image](https://user-images.githubusercontent.com/36435980/144328861-51b9d72c-1fb1-404c-810b-e3ee80a4bd1c.png)

3. Display the date in seconds since Jan 1st, 1970

![image](https://user-images.githubusercontent.com/36435980/144328897-3bf57e00-103d-47b3-8b1b-ad40b087822f.png)

4. Run the command that will show you the file type for */etc/group*

![image](https://user-images.githubusercontent.com/36435980/144328947-9ef42821-9fe0-42ee-a4d0-da7cbea248ac.png)

5. Run the command that will show you the absolute path to the command `uptime`

![image](https://user-images.githubusercontent.com/36435980/144328994-a74861d6-9642-41a9-aa49-fb80188750e6.png)

6. Determine what type of file is `uptime`

![image](https://user-images.githubusercontent.com/36435980/144329042-f25e814a-58bc-4908-a4b6-a8ddc9d8840d.png)

7. Show how many words are in the file */usr/share/dict/linux.words*

![image](https://user-images.githubusercontent.com/36435980/144329077-2f1eb0e2-3d12-4a19-a9e7-1076f0598179.png)

8. Create an alias called `utctime` that shows the time in UTC

![image](https://user-images.githubusercontent.com/36435980/144329118-6d9d006a-23f8-4087-addb-4c24bf12cec0.png)

******
<PRE>

Module_02-Documentation
├── Lesson_1
│   ├── 01-Built-in_Help
│   │   ├── 1-Shell_Built-in_Help
│   │   │   └── LAB-BASH_Builtins_Help
│   │   └── 2-External_Command_Help
│   │       └── LAB-External_Command_Help
│   ├── 02-Manuals
│   │   ├── 1-Reading_Manuals
│   │   │   └── LAB-Reading_Manual_Pages
│   │   └── 2-Searching_Manuals
│   │       └── LAB-Searching_the_Manual_Database
│   ├── 03-GNU_Info
│   │   └── 1-Reading_Info_Docs
│   │       └── LAB-Using_GNU_Info_Documentation_and_pinfo
│   └── 04-Lesson_Review
│       └── LAB-Searching_and_Using_Documentation
└── Module_Review
    └── LAB-Help_and_Documentation

</PRE>

# DOCUMENTATION
## Bultin-in Help

### TRY IT - BASH Builtins Help

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `pinfo bash `
- Navigate to the **" * Shell Builtin Commands:: "** node and press **`<ENTER>`**
- Read the first 4 paragraphs and press **`<q>`** to quit when done.
  - According to the 3rd paragraph, there are 4 groups of builtin commands that have their own documentation chapters.
- > QUESTION: What functionality do these 4 groups of builtins provide the shell?

![image](https://user-images.githubusercontent.com/36435980/144467137-88e35a0a-4ef4-4f7a-9625-8eaffb1ea17f.png)

5. `man builtins `
- > Review the list of commands in the **NAME** section of the manual that are provided as part of the shell.

![image](https://user-images.githubusercontent.com/36435980/144468391-610e487b-043f-424d-85c7-ce5572c4c07f.png)

6. `help | less `
- > QUESTION: Which of the commands listed with `help` do you use most often?

******

# DOCUMENTATION
## External Command Help

### TRY IT - External Command Help

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `mkdir --help `
- > Notice that 'Usage:' is first, followed by the default behavior of the command. 

![image](https://user-images.githubusercontent.com/36435980/144483692-7de3df31-c51d-4927-aa13-0ec88f559af6.png)

- > Full documentation is referenced at the bottom.
3. `ls --help `
- > Notice there are multiple lines of output. Scroll up in the terminal with **`<SHIFT+PG_UP>`** as needed.
4. `ls --help | less `
- > Notice that reading `--help` output through ` | less` allows searching for text and quick navigation.
5. `tar --help | head `
- > This displays just the first 10 lines of help.

![image](https://user-images.githubusercontent.com/36435980/144485101-f9fae642-8e64-4d25-abdb-4841a4ef540e.png)

6. `ls --help | grep 'sort' `
7. `grep --help | grep -i 'case' `
- > Using ` --help | grep 'string' ` displays any lines of help containing the string in single quotes.

![image](https://user-images.githubusercontent.com/36435980/144485255-68c970fa-6366-4c71-9459-47535d9b3afb.png)

******

# MANUALS
## Reading Manuals

### TRY IT - Reading Manual Pages

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `man man `
- Take a few moments to read the **DESCRIPTION** and **EXAMPLE** sections of the manual.

![image](https://user-images.githubusercontent.com/36435980/144487597-7b4402d4-49a6-4e48-9263-23a026084e26.png)
![image](https://user-images.githubusercontent.com/36435980/144487734-0051f173-fd38-475d-99ee-49d5b577cfe2.png)
![image](https://user-images.githubusercontent.com/36435980/144487794-97135955-f6c4-4149-9295-1df29e0cc615.png)

- After completing the **EXAMPLE** section, press **`<h>`** for help searching and navigating the manual.

![image](https://user-images.githubusercontent.com/36435980/144487891-80171535-cc37-46a4-b48b-22294652b03c.png)

- Press **`<q>`** to return to the manual.
- Next press the slash key **`</>`** to start a text search.
- Type `mode<ENTER>` in the search prompt to find the "Main modes of operation" section of the manual.

![image](https://user-images.githubusercontent.com/36435980/144488798-a8ed61ab-9579-4499-bc39-64f8d096150d.png)

- Refer to this section to understand the options in the **SYNOPSIS** section of the manual.
- Press **`<g>`** twice to go to the top of the manual and review the **SYNOPSIS** then press **`<q>`** to quit.

![image](https://user-images.githubusercontent.com/36435980/144489306-a73da60c-0622-4d2f-981d-e2554583bfe2.png)

3. `man -f intro `
4. `man -a intro `
- > Review the "intro" page for each section number.

![image](https://user-images.githubusercontent.com/36435980/144489466-b66e8d5f-d1c4-4acb-b49c-dce8b3661e70.png)

******

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

# GNU INFO
## Reading Info Docs

### TRY IT - Using GNU Info Documentation and `pinfo`

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Read and understand GNU INFO documentation
1. Type these commands in the terminal: 
2. `whereis pinfo `
3. `ls /usr/share/info `

![image](https://user-images.githubusercontent.com/36435980/144492624-b283b8da-c4b5-42c2-a21c-c1497691d9cd.png)

4. `pinfo  <TAB x2> `
5. `pinfo core<TAB><ENTER> `
- > Take a moment to read through the list of menu items, using the arrow keys or **`<j>`** to scroll down. 

![image](https://user-images.githubusercontent.com/36435980/144492874-e3e10118-4049-4edf-86ef-d1aaec3d1498.png)
![image](https://user-images.githubusercontent.com/36435980/144492937-ade91fed-d725-485b-b89d-b5de1ed81b7c.png)

- > Then press **`<q>`** to quit.
6. `pinfo coreutils --node="Basic operations" `
- > Take a moment to read the navigation guide at the top. 
- Press **`<n>`** to go to the next node. 
- Next press **`<u>`** to go up to the top node. 

![image](https://user-images.githubusercontent.com/36435980/144493410-9b0978ab-218a-4205-aa49-9829ac2536c6.png)

- Then press **`<q>`** to quit.)
7. `info `
- > The `pinfo` viewer may not be present on all systems. When that is the case use the `info` viewer instead. 

![image](https://user-images.githubusercontent.com/36435980/144493772-addd255b-5524-479b-afa2-737bdb3ea32e.png)

- Press **`<h>`** to view the tutorial and **`<SHIFT+H>`** to view the command keys for `info` then press **`<q>`** to quit.
	
![image](https://user-images.githubusercontent.com/36435980/144493827-ecc3aa48-caaf-43c8-820b-809d293b450b.png)
![image](https://user-images.githubusercontent.com/36435980/144493871-01dd2b47-f630-4cfc-9ad1-ea67fc3036c5.png)
	
******

# Documentation
## Lesson Review

### HANDS ON EXERCISE - Searching and Using Documentation

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter ***Passw0rd*** for the password when prompted.  
3. Type the following in the SSH terminal on server1
4. `man apropos ` 
- > Read the **DESCRIPTION** and **SEE ALSO** sections of the manual.
5. `man -k mandb `
6. `man mandb `
7. `mandb `
- > Note that user **student** does not have permission to update the manual search index.

![image](https://user-images.githubusercontent.com/36435980/144495199-d663bb92-97f0-40aa-b652-4388bdf5292d.png)

8. `sudo mandb `

![image](https://user-images.githubusercontent.com/36435980/144495290-7ffd921c-3174-44b1-8b8e-202385916c26.png)

9. `man -k mandb manuals documentation `

![image](https://user-images.githubusercontent.com/36435980/144495381-8a408d06-b6a8-43e9-8206-3c573c1f2f1f.png)

10. `man -f passwd `
11. `whatis passwd `
12. `man 5 passwd `
- > Notice section 5 covers configuration files.
13. `man 1 passwd `
- > Notice section 1 covers commands.
14. `man -K passwd `

![image](https://user-images.githubusercontent.com/36435980/144495791-c4b2acf3-425a-487e-9b53-c7f1f49ae281.png)

15. `pinfo pinfo `
- > If you want to fully understand all the keybindings in `pinfo` take a look at the "Configuration file," "Example config file" and "Keybindings" nodes.

![image](https://user-images.githubusercontent.com/36435980/144496339-146c3c00-3534-4ed3-8b3b-7755f4f23eb4.png)

16. `pinfo bash `
- Navigate to the **" \* Introduction::"** node.
![image](https://user-images.githubusercontent.com/36435980/144496516-a5a1ca57-b0e9-470c-b041-dfeb028b9b10.png)

- Read the "What is Bash?" and "What is a shell?" nodes.)
![image](https://user-images.githubusercontent.com/36435980/144496571-9a559d63-e598-4352-aaf0-d0645bed1194.png)

******

# DOCUMENTATION
## Module Review

### END OF MODULE LAB - Help and Documentation

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### TASK 3:  Perform the following operations on SERVER2

1. Update the manual page database.
2. Find out where the command `find` will execute from **and** where to find documentation in a single command.
3. Locate anything in the directory */usr/share/doc* with **README** in the name.
4. Use the manual for the `find` command and locate an **EXAMPLE** showing how to execute a command on each result found.
5. Use  ***coreutils.info*** to look up how use use the `cut` command to separate lines of text into fields.
- > Find the default *delimiter* for separating fields and the option to **override** the field delimiter.

*****

### SOLUTION

- > NOTE:  There may be many additional correct solutions other than those provided as examples in this guide.

1. Update the manual page database.

![image](https://user-images.githubusercontent.com/36435980/144499593-f17db39f-f47f-4b67-9bb8-7dcc6d070cf4.png)

2. Find out where the command `find` will execute from **and** where to find documentation in a single command.

![image](https://user-images.githubusercontent.com/36435980/144499711-1be19f8f-9629-4ff0-8055-5df83570a821.png)

3. Locate anything in the directory */usr/share/doc* with **README** in the name.

![image](https://user-images.githubusercontent.com/36435980/144499396-90e829e7-e8f9-4ea7-a492-e5d811a2c667.png)

4. Use the manual for the `find` command and locate an **EXAMPLE** showing how to execute a command on each result found.

![image](https://user-images.githubusercontent.com/36435980/144504730-045e3a67-fb62-4c69-b579-e18269a9160c.png)

5. Use  ***coreutils.info*** to look up how use use the `cut` command to separate lines of text into fields.
- > Find the default *delimiter* for separating fields and the option to **override** the field delimiter.

![image](https://user-images.githubusercontent.com/36435980/144517084-1b6beaa2-8562-482d-9f1a-295ddcb8f1c8.png)

******

<PRE>

Module_03-Working_with_Text
├── Lesson_1
│   ├── 01-The_VIM_Editor
│   │   ├── 1-Mode_Based_Operation
│   │   │   └── LAB-VIM_Basic_Navigation_and_Editing
│   │   ├── 2-EX_Mode_Basics
│   │   │   └── LAB-Saving_and_Exiting_in_VIM
│   │   └── 3-Visual_Mode_Selection_for_Copying_and_Pasting
│   │       └── LAB-Selecting_Copying_and_Pasting_in_VIM
│   └── 02-Lesson_Review
│       └── LAB-Create_and_Edit_Text_Files_Using_VIM
├── Lesson_2
│   ├── 03-IO_Redirection
│   │   ├── 1-Redirection_Symbols_and_IO_Streams
│   │   │   └── LAB-Redirecting_STDOUT_and_STDERR
│   │   └── 2-Using_Pipes
│   │       └── LAB-Using_Pipelines
│   └── 04-Lesson_Review
│       └── LAB-Using_IO_Redirection_and_Pipelines
└── Module_Review
    └── LAB-Working_with_Text
</PRE>


# THE VIM EDITOR
## Mode Based Operation

### TRY IT - Editing Text Files Using `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `vimtutor `
- Make sure the **`<CAPSLOCK>`** key is off
- Press **`<j>`** until you can see all of **"Lesson 1.1: MOVING THE CURSOR"** in the terminal.
  - Practice using the navigation keystrokes covered in **"Lesson 1.1"** until you have committed them to memory
- Use **`<j>`** to scroll down to **"Lesson 1.2."**
3. Before performing the steps in **"Lesson 1.2: EXITING VIM"** do the following tasks:
- Press **`<ESC>`** to make sure VIM is in Command Mode, a.k.a. Normal Mode.
- Type `:w ~/myvimfile.txt<ENTER> `
- > This saves the file in your home directory for later.
4. After completing step 2 of **"Lesson 1.2"** type ` vim ~/myvimfile.txt ` then resume **"Lesson 1.2"** after step 3.
- Continue the lessons down to the end of "Lesson 1.5."
- Adapt the commands in **"Lesson 1.6"** to use *~/myvimfile.txt* and read to the end of **"Lesson 1 SUMMARY."** 
5. Save your file and exit the editor.



https://user-images.githubusercontent.com/36435980/144520039-7b34ce90-987e-4478-b54b-2efce9353ac3.mp4


******


# THE VIM EDITOR
## EX Mode (Extended Command Mode) Basics

### TRY IT - Saving and Exiting in `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ls -lh > files.txt `
3. `vim files.txt `
4. Perform the following tasks in the editor:
- Press **`<ESC>`** to confirm the editor is in Command Mode.
- Type `:help<ENTER>` to view the EX Mode help
- Type `<ESC>:q<ENTER>` to leave the help and return to *files.txt*
- Type `<ESC>:help quit<ENTER>` and read down to the `ZQ` command, stopping at "MULTIPLE WINDOWS AND BUFFERS" 
5. Quit the editor without saving.


******

# THE VIM EDITOR
## Lesson Review

### HANDS ON EXERCISE - Create and Edit Text Files Using `vim`

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter ***Passw0rd*** for the password when prompted.  
3. Type the following in the SSH terminal on server1
4. `tail -n15 /usr/share/dict/words > myfile `
5. `cat myfile `
6. `less myfile `
7. While viewing *myfile* in `less`, press **`<v>`**.
- > Note that pressing **`<v>`** when reading a text file with `less` will open the file in `vim`.
8. Perform the following operations in VIM:
9. Press **`<ESC>`** then type **`<SHIFT>+<:>`** to ensure VIM is in **EX/Extended Command** mode.
10. Type **`set number`** at the EX mode prompt to turn on line numbers.
11. Press **`<gg>`** to make sure the cursor is in **position 1,1**.
12. Type **`<3yy>`** to yank a copy of the next 3 lines.
13. Type **`<2p>`** to paste 6 more lines into the file.
14.	Press **`<k>`** to move the cursor back to **position 1,1**.
15. Press **`<yy>`** to yank a copy of the top line.
16. Press **`<SHIFT>+<G>`** to go to the bottom line.
17.	Type **`<4p>`** to paste 4 more lines into the file.
18.	Type **`<3dd>`** to remove all but one of the pasted lines.
19.	Press **`<u>`** to undo the most recent change .
20.	Press **`<ESC>`** to ensure VIM is in Normal/Command mode.
21. Type **`<SHIFT>+<:>`** to switch to EX/Extended Command mode.
22. Type **`9<ENTER>`** move to line 9 from the EX mode prompt.
23.	Press **`<SHIFT>+<V>`** to switch VIM to **VISUAL LINE** mode.
24.	Type **`<5k>`** to select and highlight 5 more lines.
25.	Press **`<~>`** to change the case of the selection.
26. Type **`<gg>`** to move the cursor to **position 1,1**.
27. Press **`<CTRL>+<v>`** to switch VIM to **VISUAL BLOCK** mode.
28. Press **`<SHIFT>+<G>`** to go to the bottom line and select the first column.
29. Press **`<y>`** to yank a copy of the first column.
30. Press **`<SHIFT>+<P>`** to paste a new first column.
31. Type **`<3.>`** to repeat the last Normal/Command mode operation 3 times.
32. Press **`<SHIFT>+<G>`** to move the cursor to the last line.
33. Press **`<SHIFT>+<O>`** to open a new line in Insert mode.
34. Type in "this is some new text "
```
this is some new text
```
35.	Press **`<ESC>`** to return to Normal/Command mode.
36.	Press **`<SHIFT>+<G>`** to move the cursor to the last line again.
37.	Press **`<ESC>`** then type **`<SHIFT>+<:>`** to switch to EX mode.
38.	Type **`r  !  ls -lah `** at the EX mode prompt to insert the output of `ls -lah` at the cursor location .
39. Press **`<ESC>`** then type **`<SHIFT>+<:>`** to switch to EX mode.
40.	Type **`wq`** at the EX mode prompt to write and quit VIM returning to the earlier `less` command.
41. Press **`<q>`** to quit the `less` text pager.


https://user-images.githubusercontent.com/36435980/144658535-05020914-b121-4c24-83ff-f12274a9589d.mp4

******

# INPUT/OUTPUT REDIRECTION
## Redirection Symbols and I/O Streams

### TRY IT - Redirecting STDOUT and STDERR

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ll -R /tmp `
- > Notice some lines show files or directories - ***STDOUT*** -  while other lines - ***STDERR*** - are errors.

![image](https://user-images.githubusercontent.com/36435980/144664087-d17fa012-793b-4b5d-8faf-f7c6ac4e00c2.png)

3. `ll -R /tmp 2> /dev/null `
- > Notice the errors are discarded.
4. `ll -R /tmp &>  ~/tmpfiles1.txt `
5. `wc -l ~/tmpfiles1.txt `
- > Notice the total number of lines includes both STDOUT and STDERR.
6. `ll -R /tmp >  ~/tmpfiles1.txt `
- > Notice that STDERR goes to the terminal and STDOUT goes to the file.

![image](https://user-images.githubusercontent.com/36435980/144664146-b7ef0747-905d-4ac4-8236-d012256f4ee5.png)
		
7. `wc -l ~/tmpfiles1.txt `
- > Notice there are fewer lines.
8. `ll -R /tmp 2>  ~/tmpfiles1.txt 
- > Notice that STDOUT goes to the terminal and STDERR goes to the file.
9. `wc -l ~/tmpfiles1.txt `
- > Notice there are fewer lines.

![image](https://user-images.githubusercontent.com/36435980/144664232-7fa5f69a-0c24-4771-b98b-77c6309fa651.png)
		
10. `ll -R /tmp >>  ~/tmpfiles1.txt 2> /dev/null `
- > Notice that STDOUT goes to the file and STDERR is discarded.
11. `wc -l ~/tmpfiles1.txt `
- > Notice the lines have been appended to the file.

![image](https://user-images.githubusercontent.com/36435980/144664286-bf18d40f-e3ee-4ca4-8711-3034a0c23c67.png)

******

# INPUT/OUTPUT REDIRECTION
## Using Pipes

### TRY IT - Using Pipelines

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `wc --help `
- > Notice this line: 
```
"With no FILE, or when FILE is -, read standard input."
```
- > When a command can "read standard input" when no FILE is provided, this means you can ***pipe*** to that command.	
3. `cat /usr/share/dict/words `
- > Notice there are over 479,000 lines of output.
4. `wc -l /usr/share/dict/words `
5. `cat /usr/share/dict/words | wc -l `
- > Notice that the STDOUT of the `cat` command was read from STDIN by the command after the pipe.
6. `ll -R /tmp | wc -l `
- > Notice that STDERR goes to terminal while STDOUT goes to STDIN of the `wc` command.  
- > **STDERR must be handled before the pipe.**
7. `ll -R /tmp 2>/dev/null | wc -l `

![image](https://user-images.githubusercontent.com/36435980/144665382-d779d007-a656-4daa-bec2-49a31f0b12c2.png)
	
8. `find /usr/share/doc/ `
9. `find /usr/share/doc/ | grep 'readme' `
- > Notice only matches containing the string in quotes are shown.
10. `find /usr/share/doc/  | grep 'readme' | wc -l `
- > Counting the number of lines with `| wc -l` allows users to quickly see how many results the previous command returns.

![image](https://user-images.githubusercontent.com/36435980/144665859-2f3f6ff5-7a04-499e-93f3-85a728c21d73.png)

11. `find /usr/share/doc/  | grep --ignore-case  'readme' `
12. `find /usr/share/doc/  | grep --ignore-case  'readme' | wc -l  `
- > Notice there are many more matches for the string in quotes.

![image](https://user-images.githubusercontent.com/36435980/144666048-c903f5c3-0e5b-4ae0-959f-05991a74fb57.png)
	
13. `find /usr/share/doc/  | grep --ignore-case  'readme' | tee ~/readme_files.txt `
14. `wc -l ~/readme_files.txt `
- > Notice that STDOUT for `grep` is shown in the terminal and saved to a file when using the `tee` command.	
	
![image](https://user-images.githubusercontent.com/36435980/144666219-b2a4524b-5fec-417b-832f-77eab380aa32.png)
	
******

# WORKING WITH TEXT
## Module Review

### END OF MODULE LAB - Working with Text

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### TASK 3:  Perform the following operations on SERVER2

1. Put the first 15 lines of the file */usr/share/dict/words* into the file *~/myfile*.
2. Remove any lines that end in numbers from *~/myfile*.
3. Change all lower case letters in *~/myfile* to capital letters and change the only capital letter to lower case.
4. Find all of the **pdf** files in the file system and list the locations in a text file named *~/pdf.lst*.
5. Find all of the **jpg** files in the file system and list the locations in a text file named *~/jpg.lst*
6. Add the following host names and IP addresses to the file */etc/hosts* :
```
192.168.4.3        server1
192.168.4.4        server2
192.168.4.254      workstation
```
7. Create a file that reads "Welcome to Server 2" named *welcome.txt* in */etc/skel/* 

*****
### SOLUTION


1. Put the first 15 lines of the file */usr/share/dict/words* into the file *~/myfile*.

![image](https://user-images.githubusercontent.com/36435980/144685150-24368165-a03e-459a-80c2-29be7ece9cc8.png)

2. Remove any lines that end in numbers from *~/myfile*.
3. Change all lower case letters in *~/myfile* to capital letters and change the only capital letter to lower case.

![image](https://user-images.githubusercontent.com/36435980/144685214-7de9a856-0ccb-4846-ba7d-0a31267f06b5.png)

4. Find all of the **pdf** files in the file system and list the locations in a text file named *~/pdf.lst*.

![image](https://user-images.githubusercontent.com/36435980/144685249-30c2f6ec-5520-4c00-914e-6f4bb50b0154.png)

5. Find all of the **jpg** files in the file system and list the locations in a text file named *~/jpg.lst*

![image](https://user-images.githubusercontent.com/36435980/144685280-89183029-60ac-4fb5-bc29-dc10f75104e4.png)

6. Add the following host names and IP addresses to the file */etc/hosts* :
```
192.168.4.3        server1
192.168.4.4        server2
192.168.4.254      workstation
```

![image](https://user-images.githubusercontent.com/36435980/144685318-7465d93f-306c-4138-a5ba-1400b56fb1ab.png)

7. Create a file that reads "Welcome to Server 2" named *welcome.txt* in */etc/skel/* 

![image](https://user-images.githubusercontent.com/36435980/144685340-a0ad88d1-a856-4ddb-b481-23ae412fe0eb.png)

******

<PRE>

Module_04-Working_with_Files
├── Lesson_1
│   ├── 01-GNU_Coreutils
│   │   ├── 1-Managing_Files_and_Folders
│   │   │   └── LAB-Using_Essential_File_and_Directory_Commands
│   │   ├── 2-Using_Symbolic_Links
│   │   │   └── LAB-Using_Symbolic_Links
│   │   └── 3-Using_Hard_Links
│   │       └── LAB-Using_Hard_Links
│   └── 02-Lesson_Review
│       └── LAB-Managing_Files_Directories_and_Links
├── Lesson_2
│   ├── 03-Archiving
│   │   └── 1-Using_the_tar_Tape_Archiver
│   │       └── LAB-Tar_Archiving
│   └── 04-Lesson_Review
│       └── LAB-Managing_and_Archiving_Files
└── Module_Review
    └── LAB-Working_with_Files

</PRE>

# WORKING WITH FILES
## GNU Coreutils

### TRY IT - Using Essential File and Directory Commands

> ### Perform the following tasks on the **Workstation VM** as user **student**.

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
2. `mkdir -v  ~/classfiles `
3. `cd ~/classfiles/ `
4. `mkdir -v test1 test2 test{3..5} `
5. `rmdir -v test* `
6. `touch test-{one,two,three} `
7. `ls -lh `
8. `rm -v test-t* `
9. `ls -lh `
10. `rm -v test* `

![image](https://user-images.githubusercontent.com/36435980/145090164-4cd4ea47-0ce9-4aa6-8e58-2b2874e7f5c3.png)

11. `mkdir -v dir1 dir2 `
12. `cp -v /usr/share/dict/words  dir1/ `
13. `rmdir dir1 `
- > Read the error message.
14. `cp -v dir1/words    dir2/words2 `
15. `mv -v dir1/words   dir1/words1 `
16. `mv -v dir2    dir1/subdir `
17. `ls -lhR `

![image](https://user-images.githubusercontent.com/36435980/145090503-fc672dce-f4ba-4d29-8d66-99dc0e6238b7.png)
	
18. `rm dir1 `
- > Read the error message.
19. `rm --help | grep 'directories' `
20. `rm --recursive --verbose dir1 `
21. `cd ; pwd `
- > Make sure you are working in */home/student/* again.
22. `rmdir -v  ~/classfiles ` 

![image](https://user-images.githubusercontent.com/36435980/145090977-6a9265f1-59a5-4307-9fd7-2ba8bd8c4112.png)

******

# WORKING WITH FILES
## GNU Coreutils

## TRY IT - Using Symbolic Links

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ln --help | less `
- > Notice the usage example, default behavior, and options.

![image](https://user-images.githubusercontent.com/36435980/145092295-e390d021-46fe-4f02-af72-252264e261a6.png)

3. `file  /usr/tmp `
4. `ls -l /usr/tmp `
- > Notice there is NO TRAILING SLASH in the */usr/tmp*  path.
5. `ls -l /usr/tmp/ `
- > Notice the contents of the TARGET directory are shown with the trailing slash.
6. `cd ; pwd `
- > Make sure you are working in */home/student* first.
7. `ln  ~/Pictures   ~/Photos `
- > Notice the error message.  **Links to a directory must be symbolic.**
8. `ln  -s   ~/Pictures  ~/Photos `
9. `file Photos `
10. `stat Photos `

![image](https://user-images.githubusercontent.com/36435980/145092404-7ccf4b11-0b9b-4fad-8864-3817c9a3441f.png)

11. `sudo -i `
- > Enter ***Passw0rd*** when prompted for the password.
12. `pwd `
- > Make sure you are working in */root/* first.
13. `ln  /etc/hostname   /boot/ `   
- > Read the error message.  `"Invalid cross-device link"` means the TARGET and LINK are on different filesystems.
14. `ln -s  /etc/hostname   /boot/ ` 
15. `file   /boot/hostname  `
16. `ls -l  /boot/hostname `
17. `cat   /boot/hostname `
18. `rm   /boot/hostname `  
- > Type **`<y><ENTER>`** when prompted.   
19. `exit `
- > Return to the **student** user account.
20. `rm -v   ~/Photos `
21. `ls   ~ `

![image](https://user-images.githubusercontent.com/36435980/145093073-34e55575-0994-4dca-84d1-2b6b7501f8ec.png)

******

# WORKING WITH FILES
## GNU Coreutils

### TRY IT - Using Hard Links 

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `cd  /usr/share/zoneinfo/ `
3. `file  UTC `
4. `ls  -l /usr/share/zoneinfo/UTC `
5. `stat  UTC `
- > Notice the "link count" column from the output of `ls -l` and the "Links:" field from `stat` show the same value.
6. `find  -samefile  UTC `
7. `find  -samefile  UTC   | wc  -l `
- > Notice there are 8 hard links to the file */usr/share/zoneinfo/UTC*.
8. `ls   -li   $(  find  -samefile  UTC  ) `
- > Notice all 8 hard links point to the same **"inode"** on the filesystem.

![image](https://user-images.githubusercontent.com/36435980/145094499-d74767a0-cce3-4065-acb2-9905f8000189.png)

9. `cd ; pwd `
- > Make sure you are working in */home/student/*  again.  
10. `cp   -v   /usr/share/dict/words   ~/ `  
11. `ls   -lih ~/words `
- > Notice the inode number of *./words*.
12. `cp  -v  words   words1 ;   ls  -lih  words* ` 
- > Notice the copy has a different inode and both files have a link count of one.
13. `ln   words1   words2  ;   ls   -lih  words* `
- > Notice the link count incremented to 2 and the hard links share the same inode.
14. `ln  words1   words3  ;  ls -lih  words*  `
- > Notice the link count incremented again and the inode remains the same.
15. `rm   -v   words1    ;   ls  -lih  words* `
- > Notice the only change was the link count decreased by 1.
16. `rm   -v   words2   ;   ls   -lih   words* `
- > Notice that *words3* has a link count of 1 like a regular file.
17. `rm   -v  words* `

![image](https://user-images.githubusercontent.com/36435980/145095117-ae9cdfc4-09f9-43e9-ba05-01470b8607ce.png)

******

# GNU COREUTILS
## Lesson Summary

### HANDS ON EXERCISE - Managing Files, Directories, and Links

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm your are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Perform the following operations
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.3 `
- > Enter ***Passw0rd*** for the password when prompted.  
3. Type the following in the SSH terminal on SERVER1
4. `ls -ahl `
5. `mkdir -v  ~/lab1  ~/lab2 `
6. `cp -v /usr/share/dict/linux.words ./ `
7. `cp -v linux.words words2 `
8. `cp -v words2 lab1/words3 `
9. `ls -l lab* `

![image](https://user-images.githubusercontent.com/36435980/145096271-d12d07f8-d1df-4a12-96f1-d1523633db17.png)

10. `ln /home/student/linux.words /tmp/linux.words-HL `
11. `find  /tmp  -samefile  ~/linux.words `
12. `ls -li  /tmp  /home/student `

![image](https://user-images.githubusercontent.com/36435980/145096420-c8be16ad-d8bc-4250-bffb-4f9735df8cde.png)
	
13. `mkdir -v /home/student/lab1/lab3 `
14. `ln -s  ~/lab1/lab3  ~/lab4 `
15. `file  ~/lab4 `
16. `	tree -l  lab* ` 
17. `ls  -lhR  lab* `
18. `mv  -v  ~/words2  ~/lab4 `
19. `tree  -l   lab* `

![image](https://user-images.githubusercontent.com/36435980/145099108-32c4f79a-ad6a-4441-82df-bf7529d3380c.png)
	
20. `rm -v ~/lab4 `
21. `rm -v ~/lab1 `
22. `rm -rv  ~/lab* linux.words *.txt `

![image](https://user-images.githubusercontent.com/36435980/145099247-5e1b435a-e1dd-4fcc-8539-25f1f1c1f7f6.png)

******

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

# ARCHIVING (Pages 71-75)
## Lesson Review

### HANDS ON EXERCISE - Managing and Archiving Files

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
2. `ssh root@192.168.4.3 `
- > Enter **Passw0rd!** for the password when prompted.
3. Type the following in the SSH terminal on SERVER1
4. `hostname ; whoami ; pwd`
- > Confirm you are logged in to **SERVER1** and are starting from the **~root** home directory.
5. Open a second terminal on the **Workstation VM** as user **student** and type this command:
6. `tar --help | less `
- > Refer to this terminal for help as needed and exit `less` when done.
*****
### TASK 3: Complete the following steps on SERVER1
1. Open the ***Pearson RHCSA 8 Cert Guide*** to page 75 
2. Complete **Exercise 3-5** from the book

******

# WORKING WITH FILES (pages 62-63, 67-68)
## Module Review

### END OF MODULE LAB - Working with Files

> ### Perform the following tasks on the **Workstation VM** as user **student**.

******
### TASK 1: Confirm you are logged in to the correct host as the correct user
1. Open a terminal as needed
2. Type the following commands in the terminal:
3. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.
- > Log out and connect using the correct host and/or user as needed.
******
### TASK 2: Connect to SERVER2 as user student
1. Type these commands in the terminal: 
2. `ssh student@192.168.4.4 `
- > Enter ***Passw0rd*** when prompted.
3. Type the following commands in the terminal:
4. `hostname ; whoami ; pwd `
- > Confirm you are logged in to the correct host and starting from the the **~student** home directory.

![image](https://user-images.githubusercontent.com/36435980/144498336-a8167036-c939-4374-860c-2a720abf1ffd.png)

*****
### TASK 3:  Perform the following operations on SERVER2
1. Open the ***Pearson RHCSA 8 Cert Guide*** to pages 62-63 
2. Complete **Exercise 3-2** from the book
3. Open the ***Pearson RHCSA 8 Cert Guide*** to page 67-68
4. Complete **Exercise 3-3** from the book

******

