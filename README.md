# Useful Git Commands

#### Check version
	git --version

#### Set name and email
	git config --global user.name "Khalil Ahmed"
	git config --global user.email "mkhalila@outlook.com"

#### View config values
	git config --list

#### Help
	git help <verb> (e.g. git help config)
	git <verb> --help (e.g. git add --help)

#### Initialise a Repo from Existing code
	git init

#### Link local repo to remote repo (after creating the repo on github)
	git remote add origin https://github.com/mkhalila/<remote repo name>.git
	git push -u origin master

#### Status of repo
	git status

#### Add gitignore file (to ignore files from being tracked by Git)
	touch .gitignore

#### Add files to staging area
	git add -A
	git status

#### Commit changes
	git add -A
	git commit -m "<Commit message here>"
	git status

#### Cloning a remote repo
	git clone <url> <where to clone> ("." = current directory)
	git clone https://github.com/mkhalila/Git-Tutorials.git .

#### View branches of repo
	git branch -a

#### Submitting changes
	(Commit):
		git diff
		git status
		git add -A
		git commit -m "<Commit message>"
	(Push):
		git pull origin master
		git push origin master
    
#### See Commit History 
    git log
    ('q' to exit)

#### Create a branch
	git branch <branch-name>

#### Checkout a local branch
	git checkout <branch-name>

#### After commiting, push a new branch to remote: (First time after creating branch)
	git push -u origin <branch-name>
	git branch -a

#### Merge a branch with another branch e.g. master
	git checkout master
	git pull origin master
	git branch --merged
	git merge <branch-name>

#### Delete a branch (e.g. After merging it with master)
	git branch -d <branch-name> (deletes locally)
	git branch -a 
	git push origin --delete <branch-name> (deletes remote branch)
	
#### Update a fork with upstream changes
	git remote add upstream repo.git
	git fetch upstream
	git merge upstream/master
	git push origin

#### Reset all changes since last commit
    git reset --hard HEAD
  
#### Reset to a previous commit (need commit ID, see: `git log`)
    git reset --hard <commit-id>
  
#### Squash Commits E.g. Squash last 4 commits into a single one
    git rebase -i HEAD~4
    (pick, edit and squash appropriately, where pick is the commit you want the rest squashed into)
    Save and Exit editor
    Change commit name if necessary
    Save and Exit editor
  
#### Rename a current local branch (that hasn't been pushed yet)
    git branch -m new-branch-name
    
