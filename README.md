git config --global user.name "choudharyrahul22011"
git config --global user.email "choudharyRahul2201@gmail.com"


Set Notepad++ to path
git config --global core.editor "notepad++ -multiInst -nosession"
git config --global -e

git config --global diff.toll p4merge
git config --global difftool.p4merge.path "C:/Program Files/Perforce"
git config --global difftool.prompt false
git config --global merge.tool p4merge
git config --global mergetool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"
git config --global mergetool.prompt false


git init project-name
cd project-name

3 Local States of Git:
----------------------
Workign Directory(Were we work) When we create new file or add new file thats in Working Area, and this new file is untracked if we do git status
Staging Area(Change State) When we add it to git using command "git add file-name" or "git add ." ie all file in current dir, we move files from untrack to staging area (git status)
Repository(Git Repo for all commit changes)cwhen we do "git commit -m "message" " than files move from staging area to git repo check by git status command 

Fourth is Remote : share files by pushing to Remote System like Github

git reset HEAD FILENAME this will move the file from stage to working directory
git checkout -- FILENAME revert the changes 

git config --global alias.hist "log --oneline --graph --decorate --all"

npp example.txt create new file
git add . add new file
git commit -m "adding example.txt" commit new file
git mv example.txt demo.txt rename new file
git commit -m "rename from example to demo" commit rename of file
git rm demo.txt remove new file
git commit -m "deleting demo" commit deleting new file

npp .gitignore : Add files you want to ignore.
git add .
git commit -m "adding git ignore"

HEAD is the last commit on current branch ie if we switch branch than Head will switch and point to last commit on that branch
We can manually change the Head loacation from the last commit to some where else.

git branch
git checkout -b branch-0 create branch
npp README.md
git add .
git commit -m "updating readme to branch-0"
git status
git checkout master
git merge branch-0
git branch -d branch-0 delete branch
git branch

git tag -a v1.0 -m "Release 1.0"
git tag --list
git show

git stash used when we were changing some file and later we come to know that before this change we need to update other file first
git stash list
npp LICENCE.md update the work which you want first
git commit -am "updating licence"
git status
git stash pop once that work is done, you can pop the work from stash for commit
git commit -am "stash pop run for readme" commit stash work

git remote add origin your git url remote repo name is origin
git push -u origin master --tags remote repo name is origin and local repo which we want to push is master




























