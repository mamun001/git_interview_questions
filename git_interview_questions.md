

# .......... Git Interview Questions For DevOps Engineer OR Software Engineer  .........

## By  Mamun Rashid :: https://www.linkedin.com/in/mamunrashid/ :: Please connect with me.

### Last Updated: 2021.11.21

##

#### 1.  Imagine you join our company. We have repo that has all our Terraform codes. I asked you to create some infrastructure using Terraform. Code for that would have to go through that repo.
####     What are the steps that you would go through?


#### Answer:

       1. git clone
       2. git pull
       3. create a local branch from the Master branch or Development branch (depending on company policy)
       4. add code in that branch for this new infrastructure and create the infrastructure.
       5. commit and push the code into remote version of this new branch
       6. send in a Pull Request for merger (with master or develop)
       7. once the PR is approved, I will squash and merge 
       8. git fetch -all and git rebase

##


#### 2. You made some changes directly to develop branch and committed and pushed. Next day, you did a pull and you saw that your changes are gone. How can this happen?


#### Answer:
 
     Someone else did a push to the same branch without doing a pull first.

##


#### 3. Without knowing you made 20 changes on your local copy of the master branch. Now you have a dilemma. You don't want to push to the master branch directly (dangerous). At the same time, you also don't want to lose all these changes. What do you do?


#### Answer:

     use git stash to save your changes, pull down master branch again, create a new branch, call the stashed away changes and apply to this new branch.

##


#### 4. You ran "git checkout newbranch", but you got a funny error : something like: did not match any blah blah. What's happeing here?


#### Answer:: 

     You are trying to create a new branch. For that you need add the "-b" option

##


#### 5. git says "You ares ahead of HEAD by 1 commit". What does this mean?


#### Answer:: 

     Your local copy of the branch has 1 commit that has not been pushed to remote version of the repo.

##


#### 6. You have working on a new version of your code for hours. Now, it is a mess and you are not making any progress. You simply start over and get rid of all your uncommited changes. How do you do that?


#### Answer:: 

     git reset hard

##

### 7. You just did git fetch --all.  You like to see who has done what to this code base recently. What is a good way to see that?

#### Answer:: 

     git log

##


#### 8. What is your github ID?

#### Answer:: 

     Be ready to provide this and be sure to have to plenty of your codes in your public repo.

##



#### 9. Why would you need git rebase?

#### Answer:: 

     Use of git rebase in multi-faceted and nuanced. But, most obvious benefit is ease of reviw.

##


#### 10. Why do you need git? What problem does it solve?


#### Answer:: 

     When multiple engineers work on the same repositories, there is a need for version control, accountibility, and ability to split and merge code as needed.
     Git does those and lot more.


##


#### 11.  How do you see changes for one file only? 


#### Answer:: 

     git diff foo

##




#### 12. How do you pick only certain commits for merging two branches? 


#### Answer:: 

     git cherry-pick

##




#### 13. How do you compare two branches? 

#### Answer:: 

     git diff

##




#### 14. How do youcompare two commits?

#### Answer::  

     git diff

##


#### 15.  How can you do interactive rebase 

#### Answer:: 

     git rebase -i

##



#### 16.  What does rebase do to your branch?

#### Answer:: 

     Makes your branch look like it came from a different commit than it did originally (basically moves the marker).

##


#### 17. What is a "tag" in git?

#### Answer:: 

     git tag is like a branch that does not change. (Meant for releases) like v1.0.1.

##



#### 18. Can you "move" HEAD ?

#### Answer:: 

     Yes!

##



#### 19. What are some of the companies that host git software for us?

#### Answer:: 

     Gitlab, Github, Gerrit etc.

##


#### 20. What are two ways you can authenticate with git providers?

#### Answer:: 

     web-based user/password combo AND CLI-based using ssh

##


#### 21. Can you have more one "remote"s for your local copy?

#### Answer:: 

     Yes.

##


#### 22. You are helping a friend. He lets you have access to his terminal. The current directory is local copy of a remote git repo. BUT, he has no idea where this codebase came from. What is a good way to find that out?


#### Answer:: 

     git remote -v
     It will show which remote repos his code base came from or will push to.


##


##### 23. What command lets you create a connection between a local and remote repository?  


#### Answer:: 

     git remote add


##


#### 24. You made some changes to your local copy of the code base. You have added the new or modified files to the "staging area" using git add command. If you are done with your work, what should be your next steps?

#### Answer:: 

     git commit to commit all your changes
     git push to push your changes to the remote repo branch where it came from.

##


#### 25. When you run git commit command, how can you add a message so that everyone gets a quick summary of what changes were made or why?

#### Answer:: 

     git commit -m "some message"

##




#### 26. Can you have more than 1 stash?

#### Answer:: 

     Yes

##



#### 27. What command can your run to see the FILES in the latest stash? 

#### Answer:: 

     git stash list

##



#### 28. When you create a stash, how you give it a name?

#### Answer::  

     git stash push -m "foo"

##


#### 29. How can you restore some previously stashed work to a new branch?

#### Answer:: 

     git stash branch

##


#### 30. Your colleage just gave you access to a VM that has a local copy of repo. She did not tell you anything else. For example, are you on branch or on master? Do you have new files that are not staged? Do you have commits that have not been pushed? How can you find out all these information without any help from anyone else?

#### Answer:: 

     You can simply run "git stats".

##



#### 31. What is the difference between git fetch amd git pull ?
 
#### Answer:: 

     git fetch updates remote tracking branches with changes from a remote repository, while git pull updates remote tracking branches with changes from a remote repository and merges them into their corresponding local branches.

##


#### 32. What is the difference between git push --force and git push --force-with-lease?

#### Answer:: 

     force-with-lease is a safer option. It will not overwrite any one else's commits that have come in in the meantime.

##


#### 33. What is the difference between git log and git reflog?

#### Answer:: 

     git log shows current HEAD and its ancestry. Current commit --> it's parent -> it's parent  and so on
     git reflog does not traverse the ancestry at all. It is basically an undo path for your repo.

##


#### 34. How can you remove all untracked files?

#### Answer:: 

     git clean

##


#### 35. What if you need to examine a file line by line? 

#### Answer:: 

     git blame foofile

##


#### 36. How does git pull --rebase help?

#### Answer:: 

     It keeps history clean and avoids multiple merges

##


#### 37. "git merge foo" does what? 

#### Answer:: 

     Merges foo branch with your current branch

##


#### 38. Is there an opposite of git add?

#### Answer:: 

     Yes!  git rm

##



#### 39. How can you details about a particular commit?

#### Answer:: 

     git show commit_sha to get details on that commit

##


#### 40. git log is kind of verbose, how can you get a summarizied version?

#### Answer::  

     git shortlog to get summary of logs

##


#### 41. What command do your run to start a fesh new local repo?

#### Answer:: 

     git init

##


#### 42. Command to set up your name and your email to go with your commits?

#### Answer:: 

     git config

##



#### 43. What is so special about git bisect command when you are trying to find the buggy commit?

#### Answer:: 

    git bisect lets you choose a starting point and end point. It will let you split the difference and you decide which half has the buggy code and which one does not. It lets you keep doing this (in binary search way) until you find the buggy commit. This makes search for your buggy code much quicker.


##


#### 44. When you run git merge , what can you do so that all your micro-commits gets merged into one commit so that it is easy to read the history later on?

#### Answer:: 

     git merge --squash

##



#### 45. What is the difference between "git stash" and "git stash pop" commands?


#### Answer:: 

     "git stash" creates a stash entry (put away the files)
     BUT, "git stash pop" places the saved state onto the working directory.


#### 46. What is the difference between "git reset --soft" and "git reset -hard" ?
 
#### Answer:: 

     A soft reset only changes the commit that HEAD points to, 
     On the other hand, a hard reset resets the index and working tree to match the specified commit, discarding any changes.


#### 47. What conflicts can occur if you do a force push after rebasing?

#### Answer::  

     You can lose existing changes that's on the remote master branch. 

##


#### 48: What is trunk-based development?

#### Answer:: 

     Trunk-based development is a version control management practice where developers merge small, frequent updates to a core trunk or main branch.

##


#### 49. What is the advantage of having trunk-based development?

#### Answer:: 

     You avoid creating long-lived development branches

##


#### 50: Which command to use to see what branh you are on or to add /delete a branch?

#### Answer:: 

     git branch

##


#### 51: What is detached head state?

#### Answer:: 

     When you use git checkout to checkout a commit instead of branch.  ANy work here will not have a path back to any branch.

##


