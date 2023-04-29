## Step-by-Step instructions 
> How to create a new Git repository called `"new-project"` and a new branch called `"development"`:

Create a remote repository on the GitHub website https://github.com:

>1. Log in to your GitHub account.
>2. Select "Repositories".
>3. Select the option "Initialize this repository with a README.md file", and then click on "New" on the right side of the screen.
>4. Enter 'new-project' in the Repository name box and click on "Create repository" button.

Create a local repository on your local machine:

> Open a terminal on your computer and configure git in your local machine using the following commands: </br>
>		`git config --global user.name <username>` </br>
>		`git config --global user.email <your_email@gmail.com>` </br>


1. Create a new directory called _new-project_:

	`mkdir new-project`

2. Change to the _new-project_ directry:
	
	`cd new-project`
	
3. Initialize a new public Git repository inside the _new-project_ directory:

	`git init`
4. Create a new file called _README.md_:

	`touch README.md`
> After editing the file, save it.

5. Prepare the _README.md_ file for the commit:

	`git add README.md`

6. Commit the changes in the local repository with the commit message "init":
	
	`git commit -m "init"`

Create a link between your local Git repository and remote repository on Github to push changes to the remote repository:
```
	git remote add origin git@github.com:<username>/new-project.git` 
	git push -u origin main
```
7. Create a new branch called `development` and switch to it:

	`git checkout -b development`

> In case you need to switch from main branch to development branch, process the following command:

>	`git checkout development # from main to development branch` </br>
>	`git checkout main	  # from development to main branch`

> To check which branch you are in:

>	`git branch`

8. Add instructions to the _README.md_ file and prepare the file for commit:
> After editing the file, save it. 

	`git add README.md`
	
9. Commit the changes in the _development_ branch with the commit message:
```
	git commit -m "add instructions"
	git push -u origin development        # push the changes with the _development_ branch to the remote GitHub repository
```

10. Merge the changes from the _development_ branch to the _main_ branch:
```
	git checkout main
	git merge development 
```
11. Check status to ensure everything is up to date:
	
	`git status`

12. Commit the merging changes in the local repository:
```
	git commit -m "Merge changes from development into main branch"
	git push -u origin main`		# push the merged changes in the _main_ branch to the remote repository
```

