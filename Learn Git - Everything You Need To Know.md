https://git-scm.com/

get newest version of git
```
git clone https://github.com/git/git
```

Cheat Sheet - Courtesy of Kevin

**init** - Create an empty GIT repository in your development directory
```
Go to directory
git init
```

**status** - Show the current state of the repository including un-added and un-committed files
```
git status
```

**add** - Add a file to the repository staging area
```
Create a file, e.g. file.txt
git add file.txt
```
Add all new or changed files to the repository staging area
```
git add .
```

**commit** - Commit all changes to the repository for first time (-m means message)
```
git commit –m “Initial commit”
```

**branch** - Create a new branch of the project
```
git branch test
```

**checkout** --Switch branches and check-out all files
```
git checkout test
```
Create a new branch and check-out files in one command
```
git checkout –b test
```

**merge** - Merge two branches together (go to the destination branch first, e.g. master); merges the branch you are currently on with branchName
```
git checkout master
git merge test
```

**delete**
```
git branch test –d
```
Or to force the delete:
```
git branch test –D
```

**log** - View commit history (including long commit ID numbers)
```
git log
```

**revert** - Revert all files back to a previous commit point
```
git revert <long commit ID from the log command>
``` 

**rm -cache**  - Removes cache from a specific file so that it can be added to the .gitignore
```
git rm --cached file
```


*create new repository on github*
```
git remote add origin <url.git>
git push -u origin master
```


```
git add .
git commit -m "commit message"
git push -u origin master
```

**Cloning**
```
git clone <url.git>
```

**Basic git commands**
```
git init
git status
git add
git commit
```

**Advanced version control**
```
git branch
git checkout
git merge
git log
git revert
```

**Github**
- Adding repositories
- Cloning and updating repositories
- Readme syntax

Reference: [Udemy](https://www.udemy.com/learngit)