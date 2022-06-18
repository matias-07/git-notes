# Git Notes

- Add all tracked files modified and commit.
```bash
git commit -am "commit message"
```

- Ammend last commit.
```bash
git commit -m "commit mesage" # typo
git commit --amend -m "commit message"
```

- Show last N commits.
```bash
git log -$N # --stat / -p
```

- Revert commit X (**keeps** everything after it in history). May cause conflict.
```bash
git revert $X
```

- Reset to commit X (**deletes** every commit after X from history).
```bash
git reset --hard X
```

- Create branch from commit X.
```bash
git checkout -b $branch_name $X
```

- Create branch from current but without history (0 commits).
```bash
git checkout --orphan $branch_name
```

- Stash changes.
```bash
git stash
```

- Show stashes.
```bash
git stash show # -p
```

- Pop stash (LIFO). In case of conflict, does not drop stash.
```bash
git stash pop # pop = apply + drop
```

- Force push to remote branch.
```bash
git push -u --force origin $branch
```
