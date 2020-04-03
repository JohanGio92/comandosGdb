# Git submodules best practices

## Useful commands

— Clone repository with submodules automatically with 4 core:

`git clone --recursive --jobs=4 git@github.com:name/repo.git` 

— Initialize submodules after regular cloning:

`git submodule update --init`

— Make submodules to track their respective remote branches (instead of being in detached HEAD state):

`git submodule foreach -q --recursive 'git checkout $(git config -f $toplevel/.gitmodules submodule.$name.branch || echo master)'`

— Display status of submodules when `git status` is invoked:

`git config --global status.submoduleSummary true`

## Git Submodule by Johan

`git submodule update --init [--recursive [--remote]]`
`git push origin master --recurse-submodule=on-demand`
— Verificar que master sea trackeado al final
`git pull origin master --recurse-submodule`
— Lo hace solo para el primer nivel
`git foreach 'git chackout master'`
— Lo hace para todo los niveles
`git foreach --recursive 'git chackout master'`

## Delete submodule

1. mv a/submodule a/submodule_tmp1. git submodule deinit -f -- a/submodule
2. rm -rf .git/modules/a/submodule
3. git rm -f a/submodule# Note: a/submodule (no trailing slash)
— or, if you want to leave it in your working tree and have done step 03. 
4. git rm --cached a/submodule3bis mv a/submodule_tmp a/submodule
— then delete respectively relevant section from .gitmodules and .git/config

— Script for pulling the main repo and updating the sumodules automatically:

```bash
#!/usr/bin/env bash

git pull "$@" &&
  git submodule sync --recursive &&
  git submodule update --init --recursive
```

## Additional reading

- [Mastering Git submodules](https://medium.com/@porteneuve/mastering-git-submodules-34c65e940407)
