# Getting a repository.
You typically obtain a Git repository in one of two ways:
1) You can take a local directory that is currently not under version control, 
and turn it into a Git repository, or
2) You can clone an existing Git repository from elsewhere.

## Creating New Repo and working from commandline.

goto github and create a empty github repo.

git clone and continue

## if u already have some code

git init

goto command line on a bash shell.

echo "# urprojectname" >> README.md

git add README.md

git commit -m "first commit"

git branch -M main

git remote add origin https://github.com/rameshnagaraju/gitnotes.git

git push -u origin main

##push an existing repository from the command line

git remote add origin https://github.com/rameshnagaraju/gitnotes.git

git branch -M main

git push -u origin main

##To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

#Branching Stuff

## Listing current branches. 
git branch

##Making a new branch.
git branch <branch-name>

## Switch to new branches
git checkout <branch-name>
    
## create and change to new branch
git checkout -b newbranch

# working with remote repository

## pulling the code from remote repo

git pull origin master

## syncing with remote repository

git push origin branchname

# Adding branch name on path 

Add the following code in .bash_profile:

parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "



