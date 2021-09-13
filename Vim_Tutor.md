# Vim Tuotorial

## Part1

1. ```
   h(left)	j(down)	k(up)	l(right)
   ```

2. Quit vim

   ```
   :q!(without saving)
   :wq(save)
   ```

3. Delete characters where the cursor locates: 

   ```
   x
   ```

4. Insert the text before the cursor:

   ```
   i
   ```

   Insert the text after the cursor:

   ```
   a
   ```

   Insert the text after the end of line:

   ```
   A
   ```

## Part2

1. Delete a word from the cursor's position: 

   ```
   dw
   ```

2. Delete words from the cursor's position to the end of line: 

   ```
   d$
   ```

3. Delete the whole line: 

   ```
   dd
   ```

4. To repeat commands, add the number before commands

5. Delete commands:

   ```
   operator	[number]	motion
   Specifically:
   operator - command character, like 'd'
   [number] - additional number representing the times of the operator
   motion 	 - motion representing the command's movement on the text, like 'w'(word), $(end of line)
   
   ```

6. Move the cursor to the start of line: 

   ```
   0
   ```

7. Move the cursor to the first character of the next word:

   ```
   w
   ```

8. Move the cursor to the last character of the next word:

   ```
   e
   ```

9. Undo: 

   ```
   u
   ```

   Undo the whole operations in a line: 

   ```
   U
   ```

   Redo: 

   ```
   CTRL+R
   ```

## Part3

1. Paste the text from the buffer after the cursor : 

   ```
   p
   ```

2. Replace a character on cursor's position: 

   ```
   r
   ```

   Replace characters on cursor's position: 

   ```
   R
   ```

3. Modify commands:

   ```
   c	[number]	motion
   ```

   delete the characters from the cursor to the end of the word and go into the insert mode: 

   ```
   ce
   ```

   delete the characters from the cursor to the end of line and go into the insert mode: 

   ```
   c$
   ```

## Part4

1. Check the position of the cursor and the information of the file:  

   ```
   CTRL-G
   ```

   Jump to the last line of the file:

   ```
   G
   ```

   Jump to the specific line of the file:

   ```
   #(represent the number of the line)	G
   ```

   Jump to the first line of the file:

   ```
   gg
   ```

2. Find the string in the positive direction:

   ```
   /string
   ```

   Find the string in the opposite direction:

   ```
   ?string
   ```

   Continue searching in the postive direction:

   ```
   n
   ```

   Continue searching in the opposite direction:

   ```
   N
   ```

3. Match the brackets

   ```
   %
   ```

4. Replace one string in a line:

   ```
   :s/old_string/new_string
   ```

   Replace all strings in a line:

   ```
   :s/old_string/new_string/g
   ```

   Replace all strings between 2 lines:

   ```
   :#,#s/old_string/new_string/g
   ```

   Replace all strings in the file:

   ```
   :%s/old_string/new_string/g
   ```

   Replace all strings in the file with the permission:

   ```
   :%s/old_string/new_string/gc
   ```

## Part5

1. Operate an external command:

   ```
   !command
   ```

2. Save the editting file into a name of FILENAME:

   ```
   :w FILENAME
   ```

3. Choose the context of the file:

   ```
   v motion
   ```

   And save the context into the file:

   ```
   v motion :w FILENAME
   ```

4. Read the file and add it after the cursor

   ```
   :r FILENAME
   ```

5. Add the outputs of the command after the cursor

   ```
   :r !command
   e.g. :r !dir
   ```

## Part6

1. Open a line below the cursor in Insert mode

   ```
   o
   ```

   Open a line above the cursor in Insert mode

   ```
   O
   ```

2. Copy the selected text:

   ```
   y
   ```

   Remark: It is capable to use y as command, like $yw$ to copy a word

3. Set ignore case when finding strings:

   ```
   :set ic
   ```

   Set the founded strings highlighted:

   ```
   :set hls
   ```

   Set the strings finding instantly noticed:

   ```
   :set is
   ```

   Close the setting:

   ```
   :set noic nohls nois
   ```

   Remark: In one finding ignoring the case:

   ```
   /string\c
   ```

## Part7

1. fetch the help of Vim:

   ```
   :help
   or
   <F1>
   ```

2. Jump between different windows:

   ```
   CTRL-W	CTRL-W
   ```

3. Close the windos:

   ```
   :q
   ```

   