The GIT handbook
================

_Create a github account. Set up your username and email._
_Download and install git on your system._
_Open terminal and run:_
	git config --global user.name "Your name here"
	git config --global user.email "your_email@example.com"

0. .gitingnore file
	- The various files in your project directory that you’re not tracking in git should be indicated in a .gitignore file.
	- Tell git about the global .gitignore file:
		- git config --global core.excludesfile ~/.gitignore_global
	
1. Routine git commands
	- git add {files by name, by extension, by wildcard} # adds new, modified or deleted files to staged area and makes them ready for commit.
	- git commit -m "{message}" {staged files} # commits the staged files or files passed as argument from the staged files and creates a hashcode for revision unlinke svn
	- git push # pushes the committed revisions to the remote repository from your local repository. Do not need to do it every time. Can push after doing multiple commits.
	- git status # list of files changed, deleted, added and waiting in staging area or not.
	- git diff {filename} # all lines added to or deleted from the file
	- git pull # updates the local line of development with updates from its remote counterpart.


2. Creating a GIT repository from scratch
	- Create a directory to contain the project
	- Go into the new directory.
	- git init # git init to initialize the repository
	- Write some code
	- git add  # git add to add the files to staging area for commit
	- git commit # git commit to commit code
	
3. A new repository from an existing project
	- Go into the directory containing the project.
	- git init
	- git add (all relevant files)
	- You’ll probably want to create a .gitignore file right away, to indicate all of the files you don’t want to track. Use git add .gitignore, too.
	- git commit
	
4. Push an existing repository
	- git remote add origin https://github.com/username/new_repo
	- git push -u origin master
	
5. Create a new branch
	- git branch new_specs # creates a new branch new_specs
	- git checkout new_specs # switches to new_specs branch
	- now do you modifications then git add and git commit
	- git checkout master #jump back to the master branch
	- git push origin new_specs # pushes branch to remote

6. Merging branches
	- Merge changes made to the master into the new branch we have created.
		- git checkout new_specs
		- git merge master
	- Merge changes made to the new branch into the master branch
		- git checkout master
		- git merge new_specs
		
7. Deleting branch
	- git branch -d new_specs
	- if the branch was pushed it will still exist on github. Delete it from there:
		- git push origin --delete new_specs
