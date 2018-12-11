Git is a distributed version control system.
Git is free software distributed under the GPL.
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