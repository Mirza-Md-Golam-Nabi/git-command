# GIT-Command

## Copy or clone a GIT Repository
> `git clone repository_link`

Example: **git clone https://github.com/Mirza-Md-Golam-Nabi/git-command.git**

## Pull a branch
> `git pull origin branch_name`

Example: **git pull origin master** (branch_name = master)

## Push a branch
> `git push origin branch_name`

Example: **git push origin master** (branch_name = master)

## Temporary remove your unstaged code
> `git stash`

## Get back your stash code
> `git stash pop`

## Remove last commit from local and push it in git
> `git reset --hard HEAD~1`

> `git push origin +HEAD`

## Rollback to the last commit
> `git reflog` **To find out SHA hash number**

> `git reset --hard SHA_hash_no`

Example: **git reset --hard abc123** (SHA_hash_no = abc123) 

## Get all Branch List
> `git branch`

## Create a new branch
> `git branch branch_name`

Example: **git branch dev** (branch_name = dev)

## Create a new branch with a copy of another branch
> `git checkout -b new_branch_name copy_branch_name` **(-b = branch)**

Example: **git checkout -b dev master** (new_branch_name = dev & copy_branch_name = master)

## Delete a branch
> `git branch -d branch_name` **for soft delete**

> `git branch -D branch_name` **for hard delete**

## Delete a branch from remote
> `git push origin --delete branch_name`

Example: **git push origin --delete dev** (branch_name = dev)

## Restore your code
Restoring unstaged changes:
> `git restore .`

Unstaged your code from staged changes:
> `git restore --staged .`

Remove untracked file with directories
> `git clean -fd`
