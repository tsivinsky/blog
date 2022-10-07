# git

## useful commands

### hooks

#### how to put git hooks on GitHub

```bash
git config --local core.hooksPath [./path/to/git/hooks/dir]
```

but the thing is that every user that clones your repo should run this command. The solution is to run it with other command cloner will run anyway.

if you use npm or yarn, you can add `prepare` script with this command. now, after running `npm i` or `yarn` it will run this command.

some of the most useful git hooks (IMHO) are:
  - `precommit` to validate staged files;
  - `commitmsg` to validate commit messages;
  - `prepush` to run command before push; // building the project for example, to ensure it doesn't have any errors

### branches

#### sync cache about remote's branches in local repo

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
