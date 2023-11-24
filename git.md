# Git
## Merge your master in the current branch
```bash
git checkout <current-branch>
git merge master
```
## Merge your current changes in a different branch
```bash
git checkout <different-branch>
git add <files>
git commit -m "<message>"
git push
```
## Using submodules
```bash
git submodule init
git submodule update --recursive
# directly clone a branch with recursive submodules
git clone --recurse-submodules https://github.com/chaconinc/MainProject
```
