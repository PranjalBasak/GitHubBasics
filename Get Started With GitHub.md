# Get Started With GitHub
## Documentation
[How to Format GitHub Documents](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
## Working With Git
Development using Git follows three steps/stages. They are:
  1. **Working Directory (Use `git add` to go to the next stage):** Here we perform all the edits and create new files
  2. **Staging Area  (Use `git commit` to go to the next stage):** Before comitting, we `add` changes to the staging area, because we may not want to add every change to the staging area!
  3. **Local Repository**: By comitting, we take a permanent snapshot of the staging area's state and store in our Git repository
### Step-by-Step Procedure
  1. **Create a Local Repository**: We create a folder(Working Directory) in our machine and use `git init` to turn into a local repository
  2. **Move to the Staging Area**:
     - To add a single file to the staging area: `git add file.txt`
     - To add all files in the folder to the staging area: `git add .`
     - To check which file is in the staging area and which is not: `git status`
  3. **Move to the Local Respository**: In this stage, we commit the files/changes in the Staging Area and thus add them to the Local Repository. <br>
    `git commit -m "This is my first commit!"`
  4. **Make a Branch**: We create branches to protect our primary branch from unwanted changes. The following command will create a new branch and "check us out" on it: <br>
     `git checkout -b <new_branch_name>` <br>
     To see info about branches: `git branch`
  5. **Create a New Repository on GitHub**: Create a repository on GitHub and copy its link.
  6. **Add a Remote Repository Reference to Your Local Git Repository**: <br>
  `git remote add origin https://github.com/cubeton/mynewrepository.git` <br>
  In Git, "origin" is a conventional name for the default remote repository that your local Git repository is configured to interact with.
  7. **Push a Branch**: Pushing simply refers to updating the remote repository with your local changes(commits).
     `git push -u origin master` <br>
     **Structure**: `git push <remote> <branch>` <br>
     By using `-u` flag, you are setting up the default remote repository(upstream branch). Later you can simply, `git push` without specifying the repository name.
  8. **Pull**: Pulling will allow you to update your local branch with the remote branch. <br>
  `git pull origin master` <br>
  This command performs two actions:
    a. `git fetch` : This command retrives information on changes made on the remote repository <br>
    b. `git merge <source-branch>` : <br> First we need to switch to the target branch that will be marged with the changes from the source branch : `git checkout <target-branch>`
<br> Then we will perform the merge: `git merge <source-branch>` <br>

### Other Commands
- `git log` : This command shows the commit history of a Git repository
- `git status` : It shows the current status of your current working directory
- `git diff` : Shows the differences between your working directory and the last commit.
- `git rm file.txt` : Deletes a file from both your working directory and the staging area. You must commit to update the changes to your local respository
- `git rm -r folder`
