# Git Tutor

## Workflow

![截屏2021-09-10 10.23.27](/Users/siri/Desktop/截屏2021-09-10 10.23.27.png)

## Command

1. init a repo

   ```
   $ git init
   ```

2. add files into Stage

   ```
   $ git add <file>
   
   $ git add .					#push all files
   ```

3. commit files into History

   ```
   $ git commit -m "message"
   ```

4. Version rollback

   ```
   $ git log	[--pretty=onelin]				#fetch the history
   
   $ git reset --hard HEAD^	#reset to the last version
   
   $ git reset	--hard commit_id
   
   $ git reflog	#fetch the commit_id 
   ```

5. Check differences of files between Working Directory and Stage

   ```
   $ git diff HEAD -- <file>
   ```

6. Undo

   ```
   $ git checkout -- filename #undo the modify in Working Directory
   
   $ git reset HEAD <file> #undo the modify in Stage and put it back to the Working Directory
   ```

7. Delete

   ```
   $ rm <file>	#remove the file from Working Directory
   
   $ git rm <file> 
   $	git commit -m "message"	#remove the file from the Stage
   
   $	git checkout -- <file> #undo any file back to the Working Directory from Stage 
   ```

8. Create new repo(Github)

   ```
   $ git remote add origin www...
   $ git push -u origin master		#first time
   $ git push origin master
   ```

9. Delete remote repo

   ```
   $ git remote -v			#check the detail of remote repo
   $ git remote rm	origin	#unbound the relation between local and remote
   ```

10. Clone a remote repo

    ```
    $ git clone https://...
    ```

    