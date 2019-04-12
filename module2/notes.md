## git diff -- output change

* __git diff__: compares working directory with local repository
* __git diff --cached__: compares stage with local repository
* __git diff ./path/to/file__: scopes diff tospecified file
* __git diff branch1..other-feature-branch__: two dot op__erator compares tip of both branches
* __git diff branct1...other-feature-branch__: three dot operator changes branch1 to shared common ancestor commit between the two diff inputs and tip of other-feature-branch

* __git diff --color-words__: highlight changes for better visual
* can use homebrew pdftohtml to convert text.  
set up in ~/.gitconfig and .gitattributes

## git stash -- temporary shelving of work

* __git stash__: takes uncommited changes and saves them away for later
* __git stash -u__: stash untracked files
* __git stash -a__: stashesboth untrack and ignored files  
* __git stash -p__: partial stash allows selection of specific hunks to stash

* __git stash list__: view list of stashes
* __git stash save "text to add"__: create context when stashing
* __git stash show__: summary diff of stash
* __git stash show -p__: full diff of stash


* __git stash pop__: reapply changes to working copy and removes changes from stash
* __git stash apply__: reapply changes to working copy and keep changes in stash
* __git stash brach add-stylesheet stash@{1}__: pop first item on stash list to new branch add-stylesheet

* __git stash clear__: delete all stashes
* __git stash drop stash@{1}__: delete first item on stash list

## undoing commits and changes

* __git log <branch_name>__ : examine the log for a specific branch
* __git checkout [HASH]__: check out detached head then can run another git checkout -b new_branch to sety it as head. All future commits will no longer exist. May not be appropriate undo strategy if other code was needed.

* __git revert__: will create new commit with inverse of last commit
* __git reset__: use the --hard option will reset to specified commit should only do in local commits shared remote repo will assume push is not up to date. Use git revert instead in public repositories.
* __git commit --amend__: modify last commit message and recommit

#### git clean
* __git clean -n__: perform dry run of git clean
* __git clean -f__: execute git clean
* __git clean -d__: clean including in tracked directories
* other options: -x include ignored files -i interactive modegit revert HEAD

#### git revert
* __git revert -n__: revert without commiting. Set inverse to staging Index and Working Directory
* revert only undoes a single commit

#### git reset
* use __git ls-files -s__ to examine git staging index data
* __git reset --hard__: most dangerout as it sets working directory, staged snapshot, and commit history to reset
* __ 
* default invocation of git reset is --mixed and HEAD

## git rm: inverse of git add command
* --cached removal only on staging index not in working directory
* --ignore-unmatch exit with 0 sigterm status even if no files matched
* -q quiet hides output of git rm command

 

