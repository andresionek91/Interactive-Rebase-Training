# Interactive Rebase Training

Some exercises and training on Interactive Rebasing.

## What is rebasing?
Assume the following history exists and the current branch is "topic":
```
      A---B---C topic
     /
D---E---F---G master
```
The result of the following command:
```
git rebase master
```
would be:
```
              A'--B'--C' topic
             /
D---E---F---G master
```
## Useful `git` commands:
* `git log --oneline` Shows you git log with pretty formatting
* `git rebase -i HEAD~5` Make a list of the commits which are about to be rebased. Let the user edit that list before rebasing starting at the `5th` commit before HEAD.
* `git rebase -i <commit hash>` Make a list of the commits which are about to be rebased. Let the user edit that list before rebasing starting from the `<commit hash>`. 
* `git diff --check` Shows all lines and files with conflicts
* `git add <filename>` Adds the file back to stage after solving a conflict
* `git add -i` Interactive staging: can help you craft your commits to include only certain combinations and parts of files.
* `git rebase --abort` Undo the rebase operation
* `git rebase --continue` Resume rebase operation after fixing the conflicts
* `git push --force` Disable checks when pushing to remote repository and can cause the remote repository to lose commits; use it with care. Needed when rebasing.
