## After git is installed

### One time global Config settings

git config --global user.name "YourName"
git config --global user.email your.email@example.com

### ALIAS checkouts
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.ca 'commit --amend'
git config --global alias.st status
git config --global alias.lgo 'log --oneline'
git config --global alias.alias  'config --get-regexp ^alias\.'


### prompt branches and tab completion
#### Download files
curl -o ~/.git-completion.bash -OL cdn.learnenough.com/git-completion.bash

#### chmod to allow execution

