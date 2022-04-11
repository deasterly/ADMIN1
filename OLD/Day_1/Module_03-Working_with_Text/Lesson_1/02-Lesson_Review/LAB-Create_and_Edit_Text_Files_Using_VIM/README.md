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
