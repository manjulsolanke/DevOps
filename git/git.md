Git commands and examples
--------------------------
Here are some commonly used Git commands and examples:

revert example

1) Initializes a new Git repository in the current directory.

    `git init`

    Example: `git init`

2) Creates a copy of a remote repository on your local machine.

    `git clone` 
    
    Example: `git clone https://github.com/user/repo.git`

3) stages changes for commit.

    `git add` 
    
    Example: `git add file.txt`
             

4) Creates a new commit with the changes you have staged.

    `git commit` 

    Example: `git commit -m "Add file.txt"`

5) Displays the current state of the repository, including any changes that have not yet been committed.

    `git status` 

    Example: `git status`

6) Uploads local changes to a remote repository.

    `git push`

    Example: `git push origin main`

7) Downloads and incorporates changes from a remote repository into your local copy.

    `git pull` 

    Example: `git pull origin main`

8) Lists all branches in the repository.    

    `git branch` 

    Example: `git branch`

9) Switches to a different branch.    

    `git checkout` 

    Example: `git checkout main`
              
             `git checkout -b demo`

10) Merges changes from one branch into another.

    `git merge` 

    Example: `git merge feature-branch`

11) Displays a list of commits in the repository.

    `git log`

    Example: `git log`


12) Shows the differences between the working directory and the latest commit.

    `git diff` 
    
    `Example: git diff`


13) Lists all remote repositories.

    `git remote`

    Example: `git remote -v`


12) Downloads changes from a remote repository without merging them into your local copy.

    `git fetch`
    
    Example: `git fetch origin`


13) Resets the repository to a previous commit.
    
    `git reset`

    Example: `git reset HEAD~1`

14) Reverts a commit by creating a new commit that undoes the changes.

    `git revert`

    Example: `git revert HEAD`

15) Adds a tag to a commit to mark it as important or significant.

    `git tag` 

    Example: `git tag v1.0.0`


16) Temporarily saves changes that are not ready to be committed.

    `git stash`
    
    Example: `git stash`


17) Applies the changes of a specific commit to the current branch.
    
    `git cherry-pick`
    
    Example: `git cherry-pick 123abc`

18) Displays the details of a specific commit.    

    `git show`

    Example: `git show 123abc`


19) Configures Git settings.

    `git config` 
    
    Example: `git config --global user.name "John Doe"`

20) Shows the author and last modified time of each line of a file.

    `git blame` 
    
    Example: `git blame file.txt`

21) Displays a summary of the commit history in a single line.

    `git log --oneline`

    Example: `git log --oneline`
    
    
   Git best practices
   -------------
   
 To make the most out of Git, here are some best practices that you can follow:

1) Use branches: Create a new branch for every new feature or bug fix. This keeps your code organized and makes it easy to track changes.


2) Write good commit messages: Commit messages should be clear and descriptive, explaining what changes were made and why. This helps other developers understand your changes and makes it easier to revert changes if needed.

3) Keep commits small: Try to keep your commits small and focused on a single task. This makes it easier to understand what changes were made and helps to avoid conflicts.

4) Use pull requests: Pull requests are a great way to review and merge changes from other developers. They allow you to discuss changes, review code, and ensure that everything is working correctly.

5) Review changes before merging: Always review changes before merging them into the main branch. This helps to ensure that code quality is maintained and that changes are properly tested.

6) Use a gitignore file: Use a gitignore file to exclude files and directories that don't need to be tracked, such as build files, logs, and user-specific configuration files.

7) Keep your repository clean: Remove old branches, unused files, and other unnecessary files to keep your repository clean and easy to navigate.

8) Use tags: Use tags to mark important milestones or releases in your project.

9) Keep your repository up-to-date: Always keep your local copy of the repository up-to-date by pulling changes from the remote repository regularly.

10) Back up your repository: Back up your repository regularly to ensure that you don't lose any work in case of a disaster.

By following these best practices, you can use Git effectively and make it easier to collaborate with other developers on your project.





