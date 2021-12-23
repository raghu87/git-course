# GIT README

## Instructions for GIT

### Install Git

```bash
sudo apt update
sudo apt install -y git
```

#### Create a new repository from online

```bash
git clone https://gitlab.com/xyz/123.git
cd 123
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```

#### Push an existing folder to GIT

```bash
cd existing_folder
git init
git remote add origin https://gitlab.com/xyz/123.git
git add .
git commit -m "Initial commit"
git push -u origin master
```

#### Push an existing Git repository

```bash
cd existing_repo
git remote rename origin old-origin
git remote add origin https://gitlab.com/xyz/123.git
git push -u origin --all
git push -u origin --tags
<<<<<<< HEAD
git fetch --tags
=======
>>>>>>> 978f917d72b408438a9b2c25701ae2ec9851dee8
```

#### Configure GIT locally Usage

```bash
cd existing_repo
git config user.name "xyz"
git config user.email "xyz@xyz.com"
```

#### Configure GIT Globally Usage

```bash
cd existing_repo
git config --global user.name "xyz"
git config --global user.email "xyz@xyz.com"
```

#### Creating Branch

```bash
git branch
git checkout -b testingbranch
git push origin testingbranch
```

#### Merging testing branch to master branch

```bash
git checkout master
git merge testingbranch
git push origin master
```

#### removing branch

```bash
first switch branch
git branch
git checkout master
git branch -d stage
git push origin :stage
```

#### Creating Tags

```bash
git tag -a v1.0.0 -m"message"
forcing tag to modify
git tag -f -a v1.0.0 -m""
git push --tags
<<<<<<< HEAD
git fetch --tags
=======
>>>>>>> 978f917d72b408438a9b2c25701ae2ec9851dee8
```

#### checkout code using tags

```bash
git tag
git checkout v1.0.0
```

#### removing tags but this doesn't work on mapmyindia.gitlab

```bash
git tag -d v1.0.0
git push origin :v1.0.0
also
git tag -f -a v1.0.0 -m""
doesn't at mmi
```

#### git revert if mistakes delete happens

```bash
git checkout -- filename
```

#### Fixing the “GH001: Large files detected. You may want to try Git Large File Storage.”
```
git filter-branch -f --index-filter 'git rm --cached --ignore-unmatch fixtures/11_user_answer.json'
```

NOTE: https://en.wikibooks.org/wiki/Git/Advanced
NOTE: https://medium.com/@marcosantonocito/fixing-the-gh001-large-files-detected-you-may-want-to-try-git-large-file-storage-43336b983272




