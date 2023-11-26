# NOTE GENERATE TOKEN for lab test for myself YX
# Git commands
```bash 
git config --global user.name <name>
git config --global user.email <email>

git config --list
//Shows config

git config --global init.defaultBranch main

git init
// Initialize git repo

git status
// Checks status of repo

git add <file>
// adds file to staging area
git commit -m "message"
// Commits the files in staging area, without message will bring to vim

git diff
// see difference

git branch
// see branches
git branch <new branch>
git checkout <branch name>
// used to switch branches
git merge <branch to be merged>
// After checking out to main branch you can run merge to merge other branches

git remote add origin <url>
git remote -v
// see if its correct remote

git remote set-url origin {url}
// sets a cloned repo to a different remote

git push --set-upstream origin master 
// pushes master branch
git push -u origin

git tag -a <tag> -m <message>
git push origin <tag>

git submodule add <git submodule repo>

git clone <url of repositry to clone>

git log
```

# Git ignore
```bash
.gitignore 
//file used to ignore files
// Type file name into it and it will be ignored
```

### Add image
```md
![alt text](https://github.com/[username]/[reponame]/blob/[branch]/image.jpg?raw=true)
```