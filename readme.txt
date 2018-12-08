Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.

mkdir learngit #make new directory
cd #go to wd
pwd #show current directory
git init #make repository
git add xxxx #add xxx file to repository
git commit -m"xxxxx" #commit file to repository and add comments
git status #see current status
git diff #see difference

git log  #look at the log file to see every revise
git log --pretty=oneline  #look better log file
git reset --hard HEAD^  #back to last file version, using HEAD~100 to last 100 file 
git reset --hard commit_id  #back to future version
git reflog  #every command and commit id
cat readme.txt  #read the file and see the context