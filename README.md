# Everything about Git
A comprehensive updated crash course of Git for common everyday work.

## Setting Up and Initiating Git
Commands to set up your environment before working on a project.

`git config` - Sets up your information for your commits.
    
  ```Bash
  git config --global user.name "Lee"
  git config --global user.email "gg@gmail.com"
  ```

`git init` - Initialize a new git repository in your current folder/directory. Creates a hidden .git that tracks your project's progress/history.


`git clone <SSH or HTTPS>` - Downloads repo from a remove server to your local machine.
    
  ```Bash
  git clone git@github.com:LeejanAlipio/git-commands-test.git
  ```

`git status` - Checks the status if any changes have been made. 

`git add "The file"` - Allows you to add the file you want to the staging area. "Think of the staging area as a “waiting room” for your changes until you commit them."

`git commit -m "A description"` - Commits the files in the staging area.

`git push` - Puts the commits into the repo in GitHub, which we can see visually.

`git log` - Allows you to see the changes and who changed it.
