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
# adding submodules
git submodule add <link-to-the-repo> /path/to/submodule
```

## Reverting the changes
```bash
git log # check the commit-hash
git checkout -b new-branch-name
git cherry-pick <commit-hash>
git checkout <old-branch>
# revert by one commit
git reset --hard HEAD~1
```
## Remotes
```bash
# change the remote
git remote set-url origin https://new.url/repo.git
# Add a new branch
git checkout -b new-branch-name
git push --set-upstream origin new-branch-name
# Add a new remote branch
git remote add upstream <upstream-repo-url>
git remote -v
git fetch upstream
git checkout master
git merge upstream/master
```
## cloning
1. Set git secrets automatically:
```
sudo apt-get install libsecret-1-0 libsecret-1-dev
cd /usr/share/doc/git/contrib/credential/libsecret
sudo make
git config --global credential.helper /usr/share/doc/git/contrib/credential/libsecret/git-credential-libsecret
```
