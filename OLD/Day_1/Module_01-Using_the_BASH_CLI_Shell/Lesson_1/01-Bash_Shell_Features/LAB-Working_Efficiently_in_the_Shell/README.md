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
