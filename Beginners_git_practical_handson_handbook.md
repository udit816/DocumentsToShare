The GIT handbook
================

- _Create a github account. Set up your username and email._
- _Download and install git on your system._
- _Open terminal and run:_
	- _git config --global user.name "Your name here"_
	- _git config --global user.email "your_email@example.com"_

0. _.gitingnore file_
	- The various files in your project directory that you’re not tracking in git should be indicated in a .gitignore file.
	- Tell git about the global .gitignore file:
		- git config --global core.excludesfile ~/.gitignore_global
	
1. Routine git commands
	- _git add {files by name, by extension, by wildcard}_ adds new, modified or deleted files to staged area and makes them ready for commit.
	- _git commit -m "{message}" {staged files}_ commits the staged files or files passed as argument from the staged files and creates a hashcode for revision unlinke svn
	- _git push_ pushes the committed revisions to the remote repository from your local repository. Do not need to do it every time. Can push after doing multiple commits.
	- _git status_ list of files changed, deleted, added and waiting in staging area or not.
	- _git diff {filename}_ all lines added to or deleted from the file
	- _git pull_ updates the local line of development with updates from its remote counterpart.


2. Creating a GIT repository from scratch
	- Create a directory to contain the project
	- Go into the new directory.
	- git init # git init to initialize the repository
	- Write some code
	- _git add_ git add to add the files to staging area for commit
	- _git commit_ git commit to commit code
	
3. A new repository from an existing project
	- Go into the directory containing the project.
	- _git init_
	- _git add (all relevant files)_
	- You’ll probably want to create a .gitignore file right away, to indicate all of the files you don’t want to track. Use git add .gitignore, too.
	- _git commit_
	
4. Push an existing repository
	- _git remote add origin https://github.com/username/new_repo_
	- _git push -u origin master_
	
5. Create a new branch
	- _git branch new_specs_ creates a new branch new_specs
	- _git checkout new_specs_ switches to new_specs branch
	- now do you modifications then git add and git commit
	- _git checkout master_ jump back to the master branch
	- _git push origin new_specs_ pushes branch to remote

6. Merging branches
	- Merge changes made to the master into the new branch we have created.
		- _git checkout new_specs_
		- _git merge master_
	- Merge changes made to the new branch into the master branch
		- _git checkout master_
		- _git merge new_specs_
		
7. Deleting branch
	- _git branch -d new_specs_
	- if the branch was pushed it will still exist on github. Delete it from there:
		- _git push origin --delete new_specs_
