# git

## useful commands

### sync cache about remote's branches in local repo

if running `git branch -a` shows something like this

```bash
$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
  remotes/origin/feat/dead-branch
  remotes/origin/fix/fixed-and-merged
```

but you deleted `feat/dead-branch` and `fix/fixed-and-merged` branches using GitHub web interface, you can run the command below to update info about remote branches in your local repo.

```bash
git remote update origin --prune
```
