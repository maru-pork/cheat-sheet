```
git init
git status
dir > test1.txt
```

```
git clone <url.git>
```

*Fetch latest from master*
```
git pull origin master
```

*Add to staging*
```
git add test1.txt
git add .
```

*Commit changes*
```
git commit -m "Adding test1.txt"
```

*Add remote*
```
git remote add origin <url.git>
```

*Push to repo*
```
git push -u origin master
```

```
git config --global user.email "em@il.com"
git config --global user.name "username"
git config -l
git config --unset user.email
```
*Omit --global to set the identity only in this repository*

```
git log
git --help
```


**Branching and Merging** 

Create branch
```
git branch branchName
```  
Checkout branch
``` 
git checkout branchName 
```  
List branch
```
git branch 
```  
Push to Branch
```
git push -u origin branchName 
```  
Merge new branch in master branch
```
checkout to master first
git merge branchName
```
Push to repo
```
git push -u origin master
```
Delete branch on local
```
git branch -d name
```
Delete branch on remote
```
git push -u origin --delete name
```

**Git Tags**
- release point for a stable version
- historic point for your code/data


Checkout the branch where you want to create the tag  
```
git checkout branchname
```
Create tag with some name
```
git tag v1.0
git tag -a v1.1 -m "tag for release ver 1.1."
git tag v1.0 commitReference
```
List tag
```
git tag
git show v1.0
git tag -l "v1.*
```
Push to repo
```
git push origin v1.0
git push origin --tags
git push --tags
```
Delete tag
```
git tag -d v1.0
git push origin -d v1.0
```
Checkout certain tag from branch
```
git checkout -b branchName v1.0
```


Reference: [Udemy](https://www.udemy.com/git-and-github-step-by-step-for-beginners/)