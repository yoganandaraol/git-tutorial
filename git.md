### Initialise git branch

> git init

creates .git folder, to maintain all git related stuff

<hr />

### Branch Status

> git status

Provide you the `branch name` you are in currently.

Also let you know if any untraked and committed files/changes.

<hr />

### Stage files

> git add `filename`

Adds the specified `filename` to the committed list.

> git add . 

Stage all the changes in the `current directory`

> git add -A

Stage all the changes from the `entire repo`

<hr />

### Commit changes to local repository

> git commit -m "commit message"

commits all the changes to local repo. Commit message is used for documenting the change.

<hr />

### Commit history

> git log

Provides you the history of commits.

> git log --oneline

Provides you the history of commit details in one line for each commit.


#### Commit history - reset, revert and amend

> git reset HEAD~n

Undo the previous last `n` number of commits.
We can verify the changes using `git log` command

Also `reset` erases the change-log from commit history. In other words, we can't track down the commit history for the `reset` changes.

> git revert `commit hash`

Eg: `git rever fcd7d31`
Above is an example for reverting the specific change by change-set id (fcd7d31)

Unlike reset, revert includes the change-log to the commit history


> git commit `--amend --no-edit`

All the staged changes amend to previous commit. and `--no-edit` let's you to emend the commit without changing the commit message.

<hr />

### Branching

> git stash

Saves all untracked changes 

> git stash --list

Lists all the stashed versions

> git stash `pop`

Restores the repo with the latest stashed changes. and `removes` the stash from stash list

> git stash `apply`

Restores the repo with the latest stashed changes. and `retains` the stash from stash list

> git clean `-f`

Deletes all the untracked `files` from the local repository.

> git clean `-fd`

Deletes all the untracked `files` and `directories` from the local repository.


### Checkout branch

> git checkout -b `branch-name`

### Merge feature branch changes to master branch

> git checkout -b master

checkout master branch

> git merge feature-a

merge the feature-a branch changes into master

<hr />

> git branch --list

List all branches

> git branch -D `branch-name`

Delete the branch named `branch-name`

<hr />

### Fetch and merge remote changes

> git fetch

fetches the changes from remote.
It will not merge the fetched changes into current branch

> git merge origin/master

merges the fetched changes from remote branch into local repository

#### fetching and merging in one go

> git pull

it fecthes and merges the changes from remote into local repository

It will fetch the branch from based on the configuration detailed in following command.

> git remote -v

```bash
> git remote -v

origin	git@github.com:yoganandaraol/git-tutorial.git (fetch)<br />
origin	git@github.com:yoganandaraol/git-tutorial.git (push)
```
