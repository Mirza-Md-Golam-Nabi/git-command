# GIT-Command

## Version Check
```sh
git --version
```

Or

```sh
git -v
```

## Configure Git
```sh
git config --global user.name "nabi"
```

```sh
git config --global user.email "nabi@gmail.com"
```

## Initialize Git
To initialize a repository with the default branch named **master** :
```sh
git init
```

To initialize a repository with a branch named **main** :
```sh
git init -b main
```

## Copy or clone a GIT Repository
```sh
git clone repository_link
```

Example: **git clone https://github.com/Mirza-Md-Golam-Nabi/git-command.git**

## Pull a branch
```sh
git pull origin branch_name
```

Example: **git pull origin master** (branch_name = master)

## Push a branch
```sh
git push origin branch_name
```

Example: **git push origin master** (branch_name = master)

## Git Staging Environment

**Only for a single file**
```sh
git add file_name
``` 

**For all files**
```sh
git add --all
```

Or
```sh
git add -A
```

**For all files in shorthand**
```sh
git add .
```

## Git Commit
```sh
git commit -m "Commit Message"
```

**Git Commit without Stage**
```sh
git commit -a -m "Commit Message"
```

1. This commit works only for tracked files
2. If there are any untracked files, those files will not be added to the staging area.

## Git Status
**For Details**
```sh
git status
```

**For shorthand**
```sh
git status --short
```

Note: Short status flags are:
1. ?? - Untracked files
2. A - Files added to stage
3. M - Modified files
4. D - Deleted files

## Temporary remove your unstaged code
```sh
git stash
```

## Get back your stash code
```sh
git stash pop
```

## Remove last commit from local and push it in git remote
```sh
git reset --hard HEAD~1
```

```sh
git push origin +HEAD
```

## Rollback to the last commit
**To find out SHA hash number**
```sh
git reflog
```

```sh
git reset --hard SHA_hash_no
```

Example: **git reset --hard abc123** (SHA_hash_no = abc123) 

## Branch List
Get all local branches
```sh
git branch
```

Get all local and remote branches
```sh
git branch -a
```

## Create a new branch
```sh
git branch branch_name
```

Example: **git branch dev** (branch_name = dev)

```sh
git switch -c branch_name
```

Example: **git switch -c dev** (branch_name = dev)

## Switch a branch
```sh
git checkout branch_name
```

Example: **git checkout dev**

***N.B.*** This is old version, try to **avoid** this.

```sh
git switch branch_name
```

Example: **git switch dev**

***N.B.*** This is latest version, try to **follow** this.

```sh
git switch -
```
***N.B.*** To switch to the previous branch.

## Create a new branch with a copy of another branch

```sh
git checkout -b new_branch_name copy_branch_name
```
***N.B.*** -b = branch

Example: **git checkout -b dev master** 

```sh
git switch -c new_branch_name copy_branch_name
```

Example: **git switch -c dev master** 

new_branch_name = dev & copy_branch_name = master

## Delete a branch
**For soft delete**
```sh
git branch -d branch_name
```

**For hard delete**
```sh
git branch -D branch_name
```

## Delete a branch from remote
```sh
git push origin --delete branch_name
```

Example: **git push origin --delete dev** (branch_name = dev)

## Restore your code
Restoring unstaged changes:
```sh
git restore .
```

Unstaged your code from staged changes:
```sh
git restore --staged .
```

Remove untracked file with directories
```sh
git clean -fd
```

***N.B.*** f = Force, -d = Directories
