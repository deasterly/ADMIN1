# THE VIM EDITOR
## Visual Mode Selection for Copying and Pasting

## TRY IT - Selecting, Copying, and Pasting in `vim`

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
2. `ls -ahl > homedir.txt `
3. `vim ~/homedir.txt `
- Perform the following tasks in the editor:
4. With the cursor at **position 1,1** type **`dd`** to delete the first line.
- > Confirm your cursor position using the lower right corner of the editor window.
5. Type **`u`** to ***undo*** the change.
6. Type **`<CTRL>+r`** to ***redo*** the undone change.
7. Type **`5j`** to ***jump down*** five lines to **position 6,1**.
8. Type **`$`** to move to the end of line 6.
9. Type **`v`** to switch to **VISUAL** mode.
- > Confirm you are in VISUAL mode using the prompt in the lower left corner of the editor window.
10. Type **`gg`** to ***go*** back to **position 1,1** at the top of the document.
11. Type **`y`** to ***yank*** a copy of the selected lines and notice the prompt message.
12. Type **`<SHIFT>+P`** to ***put*** the yanked lines above the first line and notice the prompt message.
13. Type **`<ESC>:set number`** to turn on line numbers.
14. Type **`<SHIFT>+V`** to switch to **VISUAL LINE** mode and notice all of line 1 is highlighted.
15. Type **`j`** until the line for the directory *Desktop/* is highlighted.
16. Type **`r0`** to ***replace*** all the selected lines with zeros.
17. Type **`u`** to ***undo*** the previous replace operation.
18. Make sure the cursor is at **position 1,1**.
19. Type **`<SHIFT>+V`** to switch to **VISUAL LINE** mode and notice all of line 1 is highlighted.
- > Confirm you are in VISUAL LINE mode using the prompt in the lower left corner of the editor window.
20. Type **`12j`** to select the first thirteen lines.
21. Type **`x`** to ***cut*** the selected line.
22. Type **`<SHIFT>+G`** to go to the last line.
23. Type **`<ESC>:set nonumber`** to turn off line numbers.
24. Type **`dd`** to ***delete*** the last line.
25. Type **`yy`** to ***yank*** a copy of the new last line.
26. Type **`3p`** to ***put*** 3 copies of the yanked line at the bottom and notice the prompt message.
27. Type **`.`** (a dot/period) to ***repeat the last operation***.
28. Save the edited file as *~/homedir2.txt* and discard changes to the original file.
- Type **` <ESC>:wq!  ~/homedir2.txt `**



https://user-images.githubusercontent.com/36435980/144653014-189997f4-4fd5-4dea-883e-94dc7e2f2fec.mp4


******
