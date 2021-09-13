# Git Tutor

## Workflow

![截屏2021-09-10 10.23.27](/Users/siri/Desktop/截屏2021-09-10 10.23.27.png)

## Command

1. Initiate a repo

   ```
   $ git init
   ```

2. Add files into Stage

   ```
   $ git add <file>
   
   # Add all files into Stage.
   $ git add .					
   ```

3. Commit files into History

   ```
   $ git commit -m "message"
   ```

4. Version rollback

   ```
   # Fetch the history operations.
   $ git log	[--pretty=onelin]
   
   # Reset to the latest version.
   $ git reset --hard HEAD^
   
   # Reset to the specific commit_id.
   $ git reset	--hard commit_id
   
   # Fetch the history commit_id.
   $ git reflog
   ```

5. Check differences of files between Working Directory and Stage

   ```
   $ git diff HEAD -- <file>
   ```

6. Undo

   ```
   # Undo the modification in Working Directory.
   $ git checkout -- <file>
   
   # Undo the modification in Stage and put it back to Working Directory.
   $ git reset HEAD <file> 
   ```

7. Delete

   ```
   # Remove the file from Working Directory.
   $ rm <file>	
   
   # Remove the file from the Stage.
   $ git rm <file>
   $ git commit -m "message"
   
   # Undo any file back to the Working Directory from Stage.
   $ git checkout -- <file> 
   ```

8. Connect local and remote (Github)

   ```
   # Relate local repo and remote repo.
   $ git remote add origin <URL>
   ```

9. Upload files to remote library

   ```
   # For the fist time.
   $ git push -u origin master
   
   $ git push origin master
   ```

10. Delete remote repo

    ```
    # Check the details of remote repo.
    $ git remote -v	
    
    # Unbound the relation between local and remote.
    $ git remote rm	origin	
    ```

11. Clone a remote repo

    ```
    $ git clone <URL>
    ```

12. Create and switch to a branch

    ```
    # Create and switch to new branch.
    $ git checkout -b <branch_name>	
    
    # Create a new branch.
    $ git branch <branch_name>
    
    # Switch to a new branch.
    $ git checkout <branch_name>	
    
    # Create and switch to new branch with command "switch".
    $ git switch -c <branch_name>	
    
    # Switch to branch.
    $ git switch <branch_name>		
    ```

13. Check out branches

    ```
    # Branch with "*" is the temperate branch and all the modification is processed on this branch.
    $ git branch 		
    
    # Check the remote branches.
    $ git branch -r		
    ```

14. Merge branches

    ```
    # Merge the branch to the temperate one.
    $ git merge <branch_name>		 	
    ```

15. Delete branch

    ```
    $ git branch -d <branch_name>
    ```

16. Solve conflicts

    ```
    # Must modify the files to solve the conflicts manually.
    $ git log --graph		#display the graph of merging branches
    ```

17. Strategy of branches

    ```
    # The master branch must be stable, only used for releasing new versions.
    # It is recommanded to work on other branches and finally merge to the master branch.
    
    # Disable the mode of "Fast Forward", so that git will generate a new commit during merging.
    $ git merge --no-ff -m "message" <branch_name>		
    ```

18. Fix bugs

19. Save the Working Directory

    ```
    # It is recommanded to fix the bugs in a new branch.
    $ git stash
    
    # Check the stash.
    $ git stash list 	
    ```

20. Restore the Working Directory from stash

    ```
    $ git stash apply
    
    # Restore the Working Directory and clean the stash.
    $ git stash pop 	
    
    # Restore specific stash.
    $ git stash apply stash@{<number>} 
    ```

21. Clean the stash

    ```
    $ git stash drop
    ```

22. Copy the modification into the temperate branch

    ```
    $ git cherry-pick <commit_id>
    ```

23. Feature branch

    ```
    # It is recommanded to make a new branch to explore new feature.
    # Strictly delete the branch without merged
    $ git branch -D <branch_name>	
    ```

24. Team work

    ```bran
    # Push the local branch to the remote.
    $ git push origin <branch_name> 
    
    # If the push failed, try to pull the files and merge first.
    $ git pull						
    
    # Create a local branch corresponded to remote.
    $ git checkout -b <branch_name> origin/<branch_name> 
    
    # Make the relation bewteen local and remote.
    $ git branch --set-upstream <branch_name> origin/<branch_name>	
    ```

25. Add tag

    ```
    $ git tag <tag_name> [commit_id]
    
    $ git tag -a <tag_name> -m "message" [commit_id]
    ```

26. Check all tags

    ```
    # Display in the dictionary sort.
    $ git tag	
    ```

27. Check tag's details

    ```
    $ git show <tag_name>
    ```

28. Delete tag

    ```
    # Delete local tag.
    $ git tag -d <tag_name>			
    
    # Delete remote tag.
    $ git push origin :refs/tags/<tag_name>	
    ```

29. Push tag to the remote

    ```
    # Push single tag
    $ git push origin <tag_name>
    
    # Push all tags.
    $ git push origin --tags		
    ```

30. Fork a repo in Github
    ```
    1st.Fork the repo
    2nd.Clone the repo in self directory
    3rd.Back to the base repo clone the SSH 
    $ git remote add <name> <SSH>
    ```

test

