#tips and tricks
gitk - git gui
## git gr - graph view
~/.gitconfig -> [alias] -> gr = log --graph --full-history --all --color --pretty=tformat:"%x1b[31m%h%x09%x1b[32m%d%x1b[0m%x20%s%x20%x1b[33m(%an)%x1b[0m"

#created new repo via github.com
#initialize with readme/license files

#initialize local repository
git init

git add <file>
git add <directory>
git add file

git commit -m "first commit"
git commit -a 	#add and commit

git remote add origin git@github.com:<user_name>/<repo_name>.git
git push  <REMOTENAME> <TAGNAME>
git push  <REMOTENAME> --tags
git push origin master
git push origin :FIX2		#delete branch FIX2 on remote server
git push origin master		#push master branch to github
git push origin --all		#push all branches and tags
git pull origin master		#pull master branch from github
git pull origin			#pull all branches and tags

git remote -v

<repo>/.git/config – Repository-specific settings
~/.gitconfig – User-specific settings. This is where options set with the --global flag are stored
etc/gitconfig – System-wide settings

[user] 
name = John Smith
email = john@example.com
[alias]
st = status
co = checkout
br = branch
up = rebase
ci = commit
[core]
editor = vim

# basic setup at the beginning
git config --global user.name "John Smith"
git config --global user.email john@example.com

# set your text editor
git config --global core.editor vim

# add SVN looking aliases
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.up rebase
git config --global alias.ci commit

git remote
git remote -v
git remote rm paul

git clone https://github.com/{user name}/{repo name}
git clone https://github.com/patryk151900/testrepo

git checkout <commit> <file>
git checkout <commit>
git checkout master
git checkout -b <branch>

git log --oneline

git revert <commit>
git revert HEAD   -revert last change

#unpublished files only!!!
git reset <file>
git reset
git reset --hard
git reset <commit>
git reset --hard <commit>
git reset --hard HEAD~2   #remove last two commits

git clean -n	#to check what is to be removed
git clean -f

#replaces last commit
git commit --amend --no-edit	#do not change comment

#rebases to a branch
git rebase <base>	#id, branch name, tag, HEAD~x

git reflog

#merge
git merge <branch>	#from <branch> to currently pointed

#branch
git branch <branch>	#create the branch but does not switch
git branch -d <branch>	#delete the branch
git branch -v		#list the branch
git branch --merged	#only merged
git branch --no-merged	#only not merged

#ended learning on
http://git-scm.com/book/pl/v1/Ga%C5%82%C4%99zie-Gita-Zmiana-bazy

