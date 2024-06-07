# Git CheatSheet


### Main GIT Commands 

| Command       | Use               | Utility in a project 
| Git init    | initialized a local repo as a git repo | To Manage version history with git you need to declare a repository as a git repo 
| Git add       | add the changes | add the files changed. Normally use with git commit (See below). 
| Git commit | save what has been change on the local repo | Create an history of change. You can comeback to previous change if needed. Track all changes and possible errors in source code 
| Git push 
| Git pull


## Specific commands 

```sh
git push origin main 
```
> First push to repo permit to set the default branch to main (it's good practice to set default to main).

**Always Specify the branch where you push or pull. Exemple: git push origin main or git pull origin main**

```sh
git add [file.txt]
git commit --amend --no-edit 
```
> When forgetting to add a file/code to a previous commit. Re-add the file and commit what you have changes to the previous commit.


```sh
git reset --soft [shaCommit]
```
> Replace yourself at the point of the commit you specify. All the changes between the commit and now are still commited. Useful to create branch from a common base


```sh
git reset --mixed [shaCommit]
```
> Replace yourself at the point of the commit specified. All the commits between the commit and now are removed. All the changes are present


```sh
git stash [file.txt]
git stash list 
git pull origin main
git stash apply 
```
> When conflict occurs. Save all your changes locally. Get all the changes on origin main. And Re-apply your changes. 


```sh
git checkout develop
git merge feature/add-file-txt
```
> Merge all features from a branch to a common branch. 


```sh
git rebase -i HEAD~[n]

choose s to squash and p to pick the commit 

save and close 

change commit message
```
> Squash and combine multiple commit




