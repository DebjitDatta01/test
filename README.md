# test

this is for testing purpose

Using vscode for git default editor
https://stackoverflow.com/questions/30024353/how-to-use-visual-studio-code-as-default-editor-for-git

--------------------------------
first git add fileName.java (Case sensitive)

then git status(optional)

then git commit -m 'Description of update'

then git push

--------------------------------

to clone a git repo in a local machine directory 

first go to that directory 
cd /d/Study/Git

then git clone 'Git repository url link'

--------------------------------
to undo the changes in my practice.java before commit
git checkout -- practice.java

to undo all the changes that were made in local repo
git checkout -- .

to add the modified changes from my local machine to github
git add practice.java
git commit --m 'Changes name/bug fixed'
git push

--------------------------------

to undo the changes in my practice.java after commit
git log 
copy the commit id then
git revert commit_id (directly commit press :q to save)
git revert -n commit_id (no commit we need to explicitly commit again using git commit)

---------------------------------

to add all files in staging area
git add .
to remove a particular file from a staging area
git reset practice.class
to remove all from staging area
git reset
to reset from a commit_id
git reset --hard commit_id

----------------------------------
Parellel Code Development
git branching allows us to create two branches of the same code
 and then do our experiments and after testing we can merge two codes to one file

main(no longer master) is a default branch in git
to show all the branches present in repo 
git branch

to create a new branch in git 
git branch branchName
to create and also switch to the new branch
git checkout -b branchName 

to switch to a branch 
git checkout branchName

two differnt codes will be created for two differnt branches after we create new branch
so we can code in two differnt .java file and later we can merge them

to merge two files
first we need to go to main branch git checkout main
then 
git merge otherbranchName 

to push the new branch in github 
git push --set-upstream origin branchName 

to delete a branch
git branch -d branchName [this will delete from local machine only]
to delete a branch even if it is not merged
git branch -D branchName 

to delete the branch from github
after deleting from the local branch
git push origin -d branchName

-------------------------------------
head is the refernce to the latest commit (not always but in majority of the cases )
git show head 
this will show about the latest commit 
it is same as 
git show (commit_id of the last commit) 

we can use the git difftool to view differences using commit 
we can also use the head to show  older to newer
git difftool head~1 head~2
this will show the diff of  2nd and 3rd 
latest(1st) is the head  

we can change the head to ditached head using 
git chekout commit_id
or 
git checkout head~1/2/3/..
to go back to head
git checkout main 

--------------------------------------

to ignore files to apper in github repository folder 
first we need to create a gitignore file
touch .gitignore
then edit the gitignore file and add the filename
example- we can ignore all the .class files using *.class
        we can ignore a file using the full name of that file

--------------------------------------

using git difftool for diffrent editor
git difftool -t vimdiff 
git difftool -t vscode

git difftool head head~1


