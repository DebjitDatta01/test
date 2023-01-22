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
git revert <commit id> (directly commit press :q to save)
git revert -n <commit id> (no commit we need to explicitly commit again using git commit)

---------------------------------

to add all files in staging area
git add .
to remove a particular file from a staging area
git reset practice.class
to remove all from staging area
git reset
to reset from a commit id
git reset --hard <commitid>

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

to delete the branch from github
after deleting from the local branch
git push origin -d branchName

-------------------------------------
head is the refernce to the latest commit
git show head 
this will show about the latest commit 
it is same as 
git show <commit id of the last commit> 