- `git --version` -----> Checks the version of git
- `git config --global user.name "Your Name"` ----->  set your global Git user name
- `git config --global user.email "your.email@example.com"` ----->  set your global Git user email
- `git config --global user.name` -----> check for user name
- `git config --global user.email` -----> checks for user email
- `mkdir "name"` -----> create folder
- `ls` ---------------> list of the file
- `touch README.txt` --------> create file
- `cat README.txt` ----->  Displaying File Contents
- `cd ..` ----> one step previous
- `code .` -----> open vs code
- `ls -a` ------> show hidden folder 
- `git init` -> Powers your folder to be managed by git, and initialises a new empty repository. It also creates a .git folder that has all the relevant logic to manage versions of your project.
- `git status` -----> used in Git to display information about the current state of your Git repository.
- `Working Area` -> There can be a bunch of files that are not currently handled by git. It means that changes done or to be done in those files are not managed by git yet. A file which is in working area is considered to be not in the staging area. When we do git status and we see abunch if untracked files then these are actually called to be in the working area.
- `git add "file name"` -----> moves file from working area to staging area
- `Staging area` -> What all files are going to be part of the next version that we will create. This staging area is the place where git knows what changes will be done from the last version to the next version.
- `git rm --cached <file>` -----> moves file back from staging area to working area
- `Repository Area` -> This area actually contains the details of all you previous registered version. And the files in this area, git already manages them and knows their version history.
- `commit` -> Commit is a particular version of the project. It captures a snapshot of the project's staged changes and creates a version out of it.
- `git commit` -> registers staging changes to a commit.
- `git log` -> list downs all the commits of the repository. If you want to exit out of git log prompt press q.
- `git restore <file>` -> it removes all files changes from the staging area to be committed. This can be useful, if we did some dirty piece of code and now no more want it. Instead of deleting every change line by line, we can restore it or you can say restore last clean version of the file.
- `git restore --staged <file>` -> it removes file from changes from staging area to the working area. this only works if changes are in your staging area
- Diff between git rm and git restore ans: if you want to move the whole file back to the untracked state, then we do git rm, otherwise if we just want the changes to be moved in working area or staging area then we git restore.
- `git diff commit1 commit2` -> gives the difference of all file changes between two commits
- `git commit -m "<your commit message>"` -> If we want to avoid opening a text editor like vim/nano to add commit message we can use this following command
- `git remote` -> list down all the remote connection names
- Remote connection -> It helps you to link two git repositories for uploading and downloading changes from each otherwise
- `git remote add <name of remote> <link of the remote>` : this command helps us to add a new link to the remote repo and give a name to it
- `git remote rm <name of remote>` : this command deletes a remote connection
- `git remote rename <olanme> <newname>` : this command remanes the remote connection
- Note: The name of the remote connection is always used to establish communication between the repos
- `git push -u origin master` :  set up tracking and can later use git push and git pull without specifying the remote and branch.
- `git push origin master` : push the branch without setting up tracking, and you'll need to specify the remote and branch in future git push and git pull commands.
- `git add <file1> <file2> <file3>` : this command will add multiple file changes together in the staging area
- `git add .` : this command will add all files from working repo to staging area.
- `git pull <remote name> <branch name>` : downloads latest changes from the branch of the mentioned remote in your local repo.
  
## Recommended practice to do
```
- make changes
- git add <file>
- git commit 
- git pull
- git push 

```
- Merge conflicts are a very common scnario merge conflicts can occur if multiple people try to make changes to the same file, and then collaborate