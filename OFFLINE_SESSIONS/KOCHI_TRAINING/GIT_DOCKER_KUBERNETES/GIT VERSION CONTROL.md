---
created: 2024-08-19T08:53
updated: 2024-08-19T12:39
---

# Useful Git Commands List

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git init`                                                                        | Initialize a local Git repository                           |
| `git clone repo_url`                                                              | Clone public repository                                     |
| `git clone ssh://git@github.com/[username]/[repository-name].git`                 | Clone private repository                                    |
| `git status`                                                                      | Check status                                                |
| `git add [file-name]`                                                             | Add a file to the staging area                              |
| `git add -A`                                                                      | Add all new and changed files to the staging area           |
| `git commit -m "[commit message]"`                                                | Commit changes                                              |
| `git rm -r [file-name.txt]`                                                       | Remove a file (or folder)                                   |
| `git branch`                                                                      | List of branches (the asterisk denotes the current branch)  |
| `git branch -a`                                                                   | List all branches (local and remote)                        |
| `git branch [branch name]`                                                        | Create a new branch                                         |
| `git branch -d [branch name]`                                                     | Delete a branch                                             |
| `git branch -D [branch name]`                                                     | Delete a branch forcefully                                  |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git checkout -b [branch name]`                                                   | Create a new branch and switch to it                        |
| `git checkout -b [branch name] origin/[branch name]`                              | Clone a remote branch and switch to it                      |
| `git branch -m [old branch name] [new branch name]`                               | Rename a local branch                                       |
| `git checkout [branch name]`                                                      | Switch to a branch                                          |
| `git checkout -`                                                                  | Switch to the branch last checked out                       |
| `git checkout -- [file-name.txt]`                                                 | Discard changes to a file                                   |
| `git merge [branch name]`                                                         | Merge a branch into the active branch                       |
| `git merge [source branch] [target branch]`                                       | Merge a branch into a target branch                         |
| `git stash`                                                                       | Stash changes in a dirty working directory                  |
| `git stash clear`                                                                 | Remove all stashed entries                                  |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |
| `git log`                                                                         | View changes                                                |
| `git log --summary`                                                               | View changes (detailed)                                     |
| `git log --oneline`                                                               | View changes (briefly)                                      |
| `git diff [source branch] [target branch]`                                        | Preview changes before merging                              |
| `git revert commitid`                                                             | Revert commit changes                                       |
| `git config --global user.name "your_username"`                                   | Set globally Username                                       |
| `git config --global user.email "your_email_address@example.com"`                 | Set globally Email id                                       |
| `git config --global --list`                                                      | Get global config                                           |


### Getting & Creating Projects

| Command                                                           | Description                                |
| ----------------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                        | Initialize a local Git repository          |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |
|                                                                   |                                            |

### Basic Snapshotting

|Command|Description|
|---|---|
|`git status`|Check status|
|`git add [file-name.txt]`|Add a file to the staging area|
|`git add -A`|Add all new and changed files to the staging area|
|`git commit -m "[commit message]"`|Commit changes|
|`git rm -r [file-name.txt]`|Remove a file (or folder)|

### Branching & Merging

| Command                                              | Description                                             |
| ---------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |
| `git stash`                                          | Stash changes in a dirty working directory              |
| `git stash clear`                                    | Remove all stashed entries                              |

### Sharing & Updating Projects

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |

### Inspection & Comparison



| Command                                    | Description                    |
| ------------------------------------------ | ------------------------------ |
| `git log`                                  | View changes                   |
| `git log --summary`                        | View changes (detailed)        |
| `git log --oneline`                        | View changes (briefly)         |
| `git diff [source branch] [target branch]` | Preview changes before merging |
git checkout feature-branch1

git fetch --all

git pull origin main

git merge main

git commit -m "Merged main into feature-branch1"

git push origin feature-branch1  --force


git rebase main

git add <file-name>

git rebase --continue

git rebase --abort

git push --force-with-lease origin feature-branch1


**cherry pick**

git checkout feature-branch2

git log feature-branch1

git cherry-pick b6d112f34e030b6d3be5363717d495e7a14c9546

git push origin feature-branch2







