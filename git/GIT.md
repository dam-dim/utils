## For initialising a repo
This command initializes a new Git repository in your current folder.
```
git init
```

This command tells Git to save your credentials (username + personal access token) to disk for the current repository.
```
git config credential.helper store
```

This command tells Git that when you run git pull, it should merge remote changes into your local branch instead of rebasing.
Other options: merge, fast-forward
```
git config pull.rebase false
```

This command adds a remote repository to your local Git repository.
```
git remote add origin https://github.com/<username>/<repo>.git
```

This command is used to rename your current branch to main.
```
git branch -M main
```

This command links your local branch main to the remote branch origin/main so that future git pull and git push commands know where to sync.
```
git branch --set-upstream-to=origin/main main
```

## For working with a repo
This command fetches and integrates changes from the remote repository into your local branch. It’s essentially a combination of: git fetch, git merge (or git rebase)
```
git pull
```

This command stages all changes in your current directory (and subdirectories) to be included in the next commit.
```
git add .
```

This command creates a commit in your local Git repository with all staged changes with a message.
```
git commit -m "Initial commit"
```

1.  Push your local branch to the remote - Sends your commits from local main to the remote repository origin (GitHub).
2.  Set upstream tracking - “Link my local main branch to origin/main for future pulls and pushes.”. After this use git push, git pull, without a flag
```
git push -u origin main
```

## For monitoring
```
git status
git log
git log --oneline
git branch
```

## Errors
No local commits 
```
src refspec main does not match any → make a commit first
```



