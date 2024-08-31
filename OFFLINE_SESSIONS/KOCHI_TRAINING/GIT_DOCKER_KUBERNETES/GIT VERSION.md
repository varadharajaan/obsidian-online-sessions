---
created: 2024-08-19T09:07
updated: 2024-08-19T09:19
---

```
# create a git repo in a directory of your liking

mkdir gitinternals
cd gitinternals
git init -b main

## add two .txt files and commit them

echo "-TODO-" > LICENSE.txt
echo "a marcobehler.com guide" > README.txt

git add LICENSE.txt
git add README.txt
git commit -m "Project Setup"

## update README.txt's contents

echo "a git guide" > README.txt

git add README.txt
git commit -m "Updated README"

git log

git cat-file commit-id

```


Here's a table summarizing the key differences between git rebase and git merge:

| Aspect              | git rebase                                                                                                                                                                                                                                                 | git merge                                                                                                                                                                    |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Purpose             | Integrate changes from one branch into another by reapplying commits on top of the target branch.                                                                                                                                                          | Integrate changes from one branch into another by creating a merge commit.                                                                                                   |
| Resulting History   | Linear commit history, no merge commits                                                                                                                                                                                                                    | Non-linear history with merge commits                                                                                                                                        |
| Workflow            | 'Rebase and rewrite' approach                                                                                                                                                                                                                              | 'Merge and preserve' approach                                                                                                                                                |
| Complexity          | Slightly more complex, as it involves replaying commits and resolving conflicts for each.                                                                                                                                                                  | Simpler, as it involves resolving conflicts only once.                                                                                                                       |
| Conflict Resolution | Conflicts may arise and require resolution                                                                                                                                                                                                                 | Conflicts may arise and require resolution                                                                                                                                   |
| Commit IDs          | Commits get new IDs due to rewriting                                                                                                                                                                                                                       | Merge commits retain their IDs                                                                                                                                               |
| Branch History      | Creates a linear history                                                                                                                                                                                                                                   | Preserves the entire branch history                                                                                                                                          |
| Use Cases           | - Maintaining a cleaner project history  <br>- Updating feature branches  <br>- Squashing and reordering commits  <br>- Keeping feature branches up to date  <br>- Preparing code for pull requests  <br>- Ideal for individual projects/ private branches | - Preserving detailed history  <br>- Collaborative development  <br>- Merging feature branches  <br>- Hotfix integration  <br>- Collaborative development on shared branches |

Git Merge:

- Merge a branch into the current branch:

Code

```
   git merge feature-branch
```

This merges the changes from `feature-branch` into the branch you are currently on. Merge with a specific commit message.

Code

```
   git merge feature-branch -m "Merge feature-branch into main"
```

Git Rebase:

Rebase a branch onto another.

Code

```
   git checkout feature-branch   
   git rebase main
```

This rewrites the history of `feature-branch` as if it was branched off from the latest commit in `main`. Interactive rebase.

Code

```
   git rebase -i HEAD~3
```

This allows you to interactively edit, squash, or drop commits from the last 3 commits in your branch.

cherry pick commit

```

git log --all --decorate --oneline --graph

git cherry-pick commit-id

git cherry-pick --no-commit <commit SHA number>

```git
git show 2f410g1
```

git push origin cherry-pick-commit
```