# Use git reflog commands

> Here are the steps to revert to the state before a rebase using git reflog.

Run the command git reflog to display a list of past commits and operations. Each line will show a commit hash and the position of HEAD at that point.

Identify the commit hash of the state you want to revert to, which is the state before the rebase. Look through the reflog list to find the commit before the rebase was executed.
```sh
git reflog
```


Use the command git reset <commit> to move the HEAD to the state before the rebase. Replace <commit> with the hash of the commit you identified in the previous step.
```sh
git reset --soft HEAD@{n}
```
Replace n with the number of the operation in the reflog list that represents the state before the rebase. For example, if the third operation in the git reflog list represents the state before the rebase, you would run the following command:

<br>

*2023.6.15*
