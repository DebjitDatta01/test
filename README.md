# test

this is for testing purpose

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


