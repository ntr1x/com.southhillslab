# SouthHillsLab Public Site

Git super-tree

## Install shorthands

```
git config --global alias.spush 'push --recurse-submodules=on-demand'
git config --global alias.supdate 'submodule update --remote --merge'
git config --global alias.sdiff '!'"git diff && git submodule foreach 'git diff'"
git config --global alias.sstash '!'"git stash && git submodule foreach 'git stash'"
```

## Recommended commands

```
git submodule status
git submodule init
git supdate
git sdiff
git spush
git sstash
```


## Git Commands

- Check status of each submodule:

  `git submodule status`

- Fetch submodules after cloning parent module:

  `git submodule init`

- Fetch submodule updates after pulling parent module:

  `git submodule update`

- Pull submodules

  `git submodule update --remote`

- Merge submodules

  `git submodule update --remote --merge`

- Rebase submodules

  `git submodule update --remote --rebase`

- Try to push but fail if any submodule is dirty

  `git push --recurse-submodules=check`

- Push main module and submodules (All changes in submodules should be committed)

  `git push --recurse-submodules=on-demand`

- Stash all changes in submodules

  `git submodule foreach 'git stash'`

- Checkout to a new branch in all submodules

  `git submodule foreach 'git checkout -b featureA'`
