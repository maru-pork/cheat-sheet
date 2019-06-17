git commit -a -m '<commit message>'

git reset --hard

git log --oneline
git log --oneline --all
git log --oneline --all --graph

git log --no-merges

gitk --all

---
Source: https://devhints.io/git-revisions
```git
A --- E -- F -- G   master
    ¦
    +- B -- C -- D   fix
```
```git
git log master..fix	BCD
git log master...fix	BCD and EFG

git log fix..master 	EFG
git log fix...master 	BCD and  EFG
```
    $ git log --oneline --graph --all
    * d36ea0c (master) G
    * ccb98b3 F
    * bc7b928 E
    | * 3628c70 (HEAD -> fix) D
    | * d900b40 C
    | * 4b2b882 B
    |/
    * 5337149 A

```git
$ git log master..fix --oneline
3628c70 (HEAD -> fix) D
d900b40 C
4b2b882 B

$ git log master...fix --oneline
d36ea0c (master) G
ccb98b3 F
bc7b928 E
3628c70 (HEAD -> fix) D
d900b40 C
4b2b882 B
```
```git
$ git log fix..master --oneline
d36ea0c (master) G
ccb98b3 F
bc7b928 E

$ git log fix...master --oneline
d36ea0c (master) G
ccb98b3 F
bc7b928 E
3628c70 (HEAD -> fix) D
d900b40 C
4b2b882 B

******

$ git log --no-merges fix --oneline
3628c70 (HEAD -> fix) D
d900b40 C
4b2b882 B
5337149 A
103e226 another change for master
bbc5a4e made a change for master
09f18e8 Add maryannMe to README
a847148 Add maryann to README
27b93bb The initial commit of my project
```
```git
$ git log --no-merges master --oneline
d36ea0c (master) G
ccb98b3 F
bc7b928 E
5337149 A
103e226 another change for master
bbc5a4e made a change for master
09f18e8 Add maryannMe to README
a847148 Add maryann to README
27b93bb The initial commit of my project
```

Amend commit message
```git
git commit --amend
```



MERGE COMMITS 101
```git
$ git log --oneline
eb2ed9b (HEAD -> master, origin/master) add d.txt
e17649a add c.txt
3539e3f add b.txt
92cc739 add a.txt
7883dc1 Add maryann to README
27b93bb The initial commit of my project

git rebase -i HEAD~4

>reword 92cc739 add a.txt
>f 3539e3f add b.txt
>f e17649a add c.txt
>f eb2ed9b add d.txt

> add txt files

git push -u origin +master
```

```git
git branch --merged master:  lists branches merged into master
git branch --merged:  lists branches merged into HEAD (i.e. tip of current branch)
git branch --no-merged: lists branches that have not been merged

By default this applies to only the local branches. The -a flag will show both local and remote branches, and the -r flag shows only the remote branches.
```