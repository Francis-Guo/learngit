Git is a distributed version control system.
Git is a free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
Creating a new branch is quick and simple.


mkdir learngit #make new directory
cd #go to wd
pwd #show current directory
git init #make repository
git add xxxx #add xxx file to repository
git commit -m"xxxxx" #commit file to repository and add comments
git status #see current status
git diff #see difference
git diff HEAD -- readme.txt #see difference for readme text file

git log  #look at the log file to see every revise
git log --pretty=oneline  #look better log file
git reset --hard HEAD^  #back to last file version, using HEAD~100 to last 100 file 
git reset --hard commit_id  #back to future version
git reflog  #every command and commit id
cat readme.txt  #read the file and see the context

git checkout -- file  #discard changes in wd
git reset HEAD file # to unstage

git rm file #delete the file in master
git checkout -- file #discard changes in working directory

$ ssh-keygen -t rsa -C"youremail@example.com"   #set up a .ssh directory and set id_rsa
git remote add origin https://github.com/Francis-Guo/learngit.git  #connect git origin and master by using https
git remote add origin git@github.com:Francis-Guo/gitskills.git    #connect git origin and master by using ssh
git push -u origin master    #push all to origin from master; -u means connect each branch and only add in the first time
git push origin master    #push all after revising in the master

git clone git@github.com:Francis-Guo/gitskills.git    #clone repository from origin to master

git checkout -b dev   #set up a new branch dev and switch to dev, -b means start and switch to 
= $git branch dev $git checkout dev
git branch    #see all branch and current branch
git branch <name>    #set up a new branch 
git checkout <name>   #switch to branch <name>
git merge <name>    #merge <name> and master(update master)
git branch -d <name>   #delete <name>
git log --graph --pretty=oneline --abbrev-commit
git merge --no-ff -m"merge with no-ff" dev   #shut down fast forward and then merge, generate a new commit
git stash    #save current working directory
git stash list   #see what files are saved before
git stash apply    #restore working directory but not delete in stash
git stash drop     #delete the saved file in stash
git stash pop     #restore working directory and delete it in stash
git stash apply stash@{0}  #restore {0} stash

git branch -D <name>   #delete a branch which is not merged

git remote  ##check remote info
git remote -v  #check remote info details
git push origin dev  #push dev to remote origin
###must push master and dev, don't need to push bug, feature branch depends on if someone develop with you
git clone git@github.com:michaelliao/learngit.git   #only clone master
git checkout -b dev origin/dev  #set up origin dev to local

git pull  #pull a branch to local
git branch --set-upstream-to=origin/<branch> dev   #if you wish to set tracking information for this branch you can do so with
git branch --set-upstream-to=origin/dev dev

git rebase    #rebase the log 
git tag <name>   #tag to commit
git tag    #see all tags

git tag v0.9 26b59ec  #tag history commit
git show <tagname>   #show tagname details
git tag -a v0.1 -m "version 0.1 released" e67573e    #-a: tagname  -m:details

git tag -d <tagname>  #delete wrong tag
git push origin <tagname>    #push tag to origin
git push origin --tags   #push all unupload tags to origin
git push origin :refs/tags/<tagname>   #delete wrong tag in origin

git config --global color.ui true   #show color in git bush
git config --global alias.st status  #use st represent status


