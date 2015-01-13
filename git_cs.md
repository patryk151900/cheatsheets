#created new repo via github.com
#initialize with readme/license files

#initialize local repository
git init

git add <file>
git add <directory>
git add file

git commit -m "first commit"

git remote add origin git@github.com:<user_name>/<repo_name>.git
git push origin master

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

git push  <REMOTENAME> <TAGNAME>
git push  <REMOTENAME> --tags
git push origin master

git remote
git remote -v
git remote rm paul

git clone https://github.com/{user name}/{repo name}
git clone https://github.com/patryk151900/testrepo

git checkout <commit> <file>
git checkout <commit>
git checkout master

git log --oneline

git revert <commit>
git revert HEAD   -revert last change



























