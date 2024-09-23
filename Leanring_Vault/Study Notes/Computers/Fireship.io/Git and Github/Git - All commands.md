## git init 
- initialize a repo within a folder

## git status
- check the status
- which files have been added, deleted, modified and so on

## .gitignore file
- in gitignore, add the file name inside of it.
	- save file, and do `git status`
	- status should not show the file when listing out all files


## 3 file areas of a git
- working dir
	- currently looking at
- staging area
	- `git add` puts files here
- commits

## Staging 
- a concept
	- you have to add some files to the "stage" before you commit the repo
## git add 
- `git add .`  = add all files in the working directory 
- `git add {filename}` = add file to be prepared for commit

## git commit
- `git commit -m "{message}" `
-  -a = all files in the working directory
	- `git commit -am "message" `
- *don't have to do git add -> git commit to every file, esp those that exist in the repo and are just modified*

## git log
- shows the log of the commit
	- who made it
	- on what date
	- unique commit ID
- `git log --graph --oneline --decorate`
	- shows a nicer version of the timeline of commits


## git remote
- many options to store your repos, like github
	- can make a new repo - copy the url of repo (once you set it up)
- `git remote` = tells which remote repos you have linked to your local projects 
- `git remote add {name_of_repo} {url_to_repo}` 
	- `git remote add origin https://github.com/codeiodeio/test-repo.git`
- now `git remote` will show you the connected repo

## git push
- `git push {name_of_remote_repo} {branch_to_push} (-u)`
	- `git push origin master -u`
	- -u = set *origin* to upstream remote
		- allows to use `git pull` wo/ additional args


## difference in changes
- say that you changed a simple typo directly in GitHub and commit that change.
	- now your online repo is ahead of your local repo by 1 commit
- how do you make sure that you have the same commit on local?
## git fetch 
- grab the *remote branch* of the repo / meaning the one online
- `git fetch
- then do a merge 
## git merge
`git merge {branch_to_merge}`
- `git merge origin/master`

## git pull
fetch + merge
- `git pull origin master`
	- but since we did the `-u` flag earlier, we can just say `git pull` 
- if you have unsaved changes in your local directory, pull will fail
	- a. commit local changes first 
	- b. or stash it (advanced)
- if your local change is also editing the same code that your pulling, you will get an error 


## git clone
- `git clone {url_to_repo} (name_for_directory)`
	- `git clone https://github.com/fireship.io/next-firebase-course.git demo`

## code spaces
- allows you to run the code in the cloud, paid for per second spent


## git branch
![[Pasted image 20240903144849.png]]
*branches allow for ppl to collaborate with each other wo/ getting in the person's way*

- `git branch`
	- shows branches
- `git branch -M main`
	- rename master branch to "main"
- `git branch awesome`
	- create a new branch (**not in it yet**)
- `git branch -d awesome`
	- delete a branch

## git checkout
- go into a branch
- `git checkout {branch_name}`
	- `git checkout awesome`
- to create a new branch and checkout into it at the same time:
	- `git checkout -b {branch_name}`
- `git checkout -` = checkout to previously used branch

## merge conflicts
- occur when you try to merge 2 diff branches and they modify the same code
- `git diff`
	- look at the difference btwn 2 files
- `git merge --abort`
	- if unsure which change to make, you can abort the merge

## fork
- more so a github thing
- allows you to copy someone's repo and work on it within your account
	- original repo you copied = "upstream"
- you can then send a pull request to the original author 
	- submit changes so that author can approve it 


## git reset 
- `git reset` = remove all files from the staging area, will not delete them
- let's say you made a commit with a bad file and want to go back a commit
	- `git reset {commit_ID}`
		- does so in mixed mode, meaning that previous version came back, but other files haven't been deleted
	- `git reset --hard {commit_ID}`
- best practice, if already pushed to remote repo (github), best to leave it - bc other devs may need it 


## git revert
- get the commit_ID of the bad push 
- `git revert {bad_commit_ID}`
	- reverts the remote repo, but doesn't hard delete the file. 
		- instead it is saved in history

## git commit --amend
#### git commit --amend -m "new message"
- changes the message of the most recent commit

say that there's a staging file that you might've forgotten, you can add it to the most recent commit wo/ creating a new commit
- `git add {filename}`
- `git commit --amend --no-edit`


## git stash
- save your work for later wo/ commiting it
- `git stash` = saves file to stash; stash is kinda like an array
	- `git stash pop` =  bring back the edited stash 
- `git stash save {save_name}`
	- keep track of stashes
- `git stash list`
	- shows diff changes w/ index
-  `git stash apply {index}`

## git rebase
 ![[Pasted image 20240903165640.png]]
- does re-write history, so you can't rollback to before the rebase



## git squash
- squash multiple commits into a single commit
![[Pasted image 20240903170012.png]]
*change pick to squash*
*another file will open - asking to write out any comments*


## alias
- create a shortcut for yourself 
	- `git config --global alias.{command_name} "{command}"`
		- `git config --global alias.ac "commit -am" `

## hooks
- allow to run code before or after an event
	- ex: making a commit creates an event, a hook can run either before or after that commit

