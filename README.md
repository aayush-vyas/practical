# Practical
# 1. Pull and Merge difference
first of all i have created one text file in main branch called new.txt. then after created one branch called "feature-a", and made some changes in new.txt from the feature-a branch.
then i made pull request and merge it to main branch.

some of the command i had used for it.
``` 
1. git add .
2. git commit -m "new file added"
3. git push origin master
4. git checkout -b feature-a
# made some changes in new.txt from feature-a
5. git checkout master
6. git merge feature-a

```

# 2. Rebase 
then after i have created one more branch called feature-rebase. and applied some changes in new.txt from feature-rebase branch. and checkout to master and then rebase master into feature-rebase

```
1. git checkout -b feature-rebase
# made some changes in new.txt
2. git checkout master
3. git rebase feature-rebase
```

# 3. Change commit message
```
1. git checkout feature-rebase
2. git commit --amend 
```

# 4. Cherry pick
 I switch to feature-rebase, and created one more file called new_com_change.txt, made some changes, commited two times. and then cherry-picked first commit from master branch
 
 ```
 1. git checkout feature-rebase
 2. git commit -m "cherry-pick 1"
 #did some changes.
 3. git commit -m "cherry-pick 2"
 4. git checkout master
 5. git cherry-pick id_of_commit
 
 ```
 
 # 5. Drop commit
```
1. git checkout feature-rebase
2. git reset --hard HEAD~1
3. git push origin HEAD --force 
```
