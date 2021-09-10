# Git Tutor

## Workflow

![截屏2021-09-10 10.23.27](/Users/siri/Desktop/截屏2021-09-10 10.23.27.png)

## Command

1. Initiate a repo

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
   $ git commit -m "message"	#remove the file from the Stage
   
   $ git checkout -- <file> #undo any file back to the Working Directory from Stage 
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

11. Create and switch to a branch

    ```
    $ git checkout -b <branch_name>	#create and switch to new branch
    
    $ git branch <branch_name> 		#create a new branch
    $ git checkout <branch_name>	#switch to a new branch
    
    $ git switch -c <branch_name>	#create and switch to new branch with command "switch"
    $ git switch <branch_name>		#switch to branch
    ```

12. Check out branches

    ```
    $ git branch
    #branch with "*" is the temperate branch and all the modify is dued on this branch
    ```

13. Merge branches

    ```
    $ git merge branch_name		 	#merge the branch to the temperate one
    ```

14. Delete branch

    ```
    $ git branch -d branch_name
    ```

15. Solve conflicts

    ```
    # Must modify the files to solve the conflicts manually
    $ git log --graph		#display the graph of merging branches
    ```

16. Strategy of branches

    ```
    # The master branch must be stable, only used for release new versions.
    # It is recommanded to work on other branches and finally merge to the master branch.
    
    $ git merge --no-ff -m "message" <branch_name>		# disable the mode of Fast forward, so that git will generate a new commit during merging.
    ```

17. Fix bugs

    ```
    $ git stash				#save the temperate Working Directory
    
    # It is recommanded to fix the bugs in a new branch
    
    $ git stash list 	#check the stash
    
    $ git stash apply #restore the working directory
    $ git stash drop 	#clean the stash
    
    $ git stash pop 	#restore the working directory and clean the stash
    
    $ git stash apply stash@{number} #restore specific stash
    
    $ git cherry-pick <commit_id>	#copy the modify into the temperate branch
    ```

    

    