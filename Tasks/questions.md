### Answer the following questions in you own words.

> It's not necessary that you havee to know and answer all the questions. Just answer the ones
> you know and write in your own words.

1. Give the difference between the remotes - upstream and origin - with an example.
       
You answer: 
 
             origin is the remote name given to the repo you clone (usually your fork).

             upstream is added to track the original repo you forked from, so you can stay updated.

             example : 

             git remote add upstream https://github.com/org/vedant.git
              
             Here, origin might be your fork, and upstream is the main project.

2. You have two branches A and B and you have currently made some changes in branch A.
You want to move into branch B but do not want to commit the current changes in branch A.
What will you do?

You answer:  
        
            If I made changes in branch A but don’t want to commit yet, I can stash them using -  git stash . after this we can do checkout B to switch to the branch B . This saves my changes and lets me move to branch B. Later, I can get them - back with git stash pop . 

3. You were assigned a work to implement a feature and create a PR to your organization's remote repository.
For this you made a branch (say A) and made some changes and commited them. Now you moved to some other branch 
(say B) to do some other assigned work. But later you realisd that have to complete the task assigned earlier 
first and commited some changes in branch B which are meant for branch A. How will you use git to bring the 
changes from branch B to branch A?

You answer:
           
           First, I’d note down the commit hash of the wrong commit I made in branch B. You can see the commit hash by running - git log .
           Then, I’d switch back to branch A (the branch where the commit was actually supposed to go) - git checkout A . 
           Now I’d use git cherry-pick with that commit hash - git cherry-pick <commit_hash> 
           This way, the commit I accidentally made in B will now also appear in A, which is where it should have been in the first place.

            If I don’t want that commit in branch B anymore, I can also go back to branch B and remove it using  - git reset --hard HEAD~1


3. What is the difference between fetching changes and pulling changes?

Your answer:
           
           git fetch only downloads updates from the remote repo, but doesn’t change my working branch.
           git pull does a fetch and merges the changes into my current branch directly.


4. What does -i flag stand for? What is it's significance in git?

You answer: 
         
          The -i flag stands for interactive.
          It’s most useful in git rebase -i, which lets me squash, edit, or reorder commits before pushing them.

5. You are working in an organization that follows very strict guidelines for PRs and commits.
You made three commits in your PR and the maintainer says you were supposed to make a single commit.
What will you do in this case?

You answer:
          
          If I made 3 commits but should have only 1, I woud squash them using - git rebase -i HEAD~3 . 
          Mark the last two as squash (s). Now, all 3 become 1 commit.
          Finally, I force-push - git push origin branchname --force . 

6. Explain `git merge` and `git rebase` with example(s).

You answer: 
       
          Merge: Combines two branches and creates a new merge commit. Example: if main has commits A–B–C and feature has D–E, then after merging, history shows both branches joined together with a merge commit.

          Rebase: Moves the commits of one branch on top of another to make history linear. Example: if main has A–B–C and feature has D–E, after rebasing, history looks like A–B–C–D–E, as if feature started from the latest main.
          merge keeps complete history , whjile rebase makes it clean .
        

7. Write the flow how you create a repository and push changes to it. Also mention the commands used at each step.

You answer:  
           initialise a repo . git init 
           add a remote o connect local repo to git  . git remote add origin repolink.git
           git add . 
           git commit -m "commit message " 
           git push -u origin main 



8. How would you prevent a file or folder from getting tracked by git?

Your answer: to prevent Git from tracking files by adding them to a .gitignore file. used for node modules , .env files . 

9. You did not implement the step you mentioned in question 8 and now you have committed and pushed your database's
secret key to the github. How will you remove the key from your git's commit history to avoid any misuse?

You answer:  
           git reset --hard HEAD~1
           git push origin --force
           also we need to create a new key in case the previous one is exposed globally . 

---